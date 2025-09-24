# Dify Dokploy Deployment Guide

このガイドでは、DifyをDokployでデプロイするための手順と設定について説明します。

## 前提条件

- Dokployがインストールされていること
- Dockerが利用可能な環境であること
- 十分なリソース（CPU、メモリ、ディスク容量）があること

## デプロイ手順

### 1. 環境設定

1. `docker/middleware.env.example` を `.env` にコピーします
2. 必要な環境変数を設定します：
   - `CONSOLE_API_URL`: コンソールAPIのURL（https://dify.hyper-typer.xyz/console/api）
   - `CONSOLE_WEB_URL`: コンソールWebのURL（https://dify.hyper-typer.xyz/console）
   - `APP_API_URL`: アプリケーションAPIのURL（https://dify.hyper-typer.xyz/v1）
   - `APP_WEB_URL`: アプリケーションWebのURL（https://dify.hyper-typer.xyz/app）
   - `SECRET_KEY`: 強力なシークレットキー（openssl rand -base64 42 で生成）
   - `INIT_PASSWORD`: 管理者パスワード
   - `NGINX_HTTPS_ENABLED`: true（Cloudflare Tunnel用）
   - その他の必要な設定

### 2. Dokployでの設定

1. **Serviceの作成**:
   - Dokployのダッシュボードにアクセス
   - "Create Service" をクリック
   - Service Type: Docker Compose
   - Upload docker-compose.dokploy.yaml

2. **Environment Variables**:
   - .env ファイルの内容をEnvironment Variablesとして設定
   - 各環境変数を確認・修正

3. **Port Configuration** (Cloudflare Tunnelを使用する場合):
   - **Cloudflare Tunnel専用**: 外部ポート公開は不要
   - **ローカルテストの場合のみ**:
     - **Add Port**: 80 (Nginx HTTP)
     - **Host**: 0.0.0.0
     - **Container Port**: 80

4. **Network**:
   - Network Mode: Bridge
   - 外部ネットワーク `dokploy-network` が存在することを確認

5. **Volumes**:
   - 必要なボリュームが自動的に作成されることを確認
   - データ永続化のためのボリューム設定

6. **Networking**:
   - 外部ネットワーク `dokploy-network` が存在することを確認
   - 必要に応じてネットワーク設定を調整

### 3. Cloudflare Tunnel設定（必須）

Cloudflare Tunnelを使用する場合：
1. **Cloudflare Dashboard**でTunnelを作成
2. Tunnelのドメインを `dify.hyper-typer.xyz` に設定
3. **Public Hostnameの設定**:
   - **Domain**: `dify.hyper-typer.xyz`
   - **Service**: `http://localhost:80` ← **重要：DokployのNginxコンテナの内部URL**
   - **Path**: `/`（空のまま）
   - **HTTP/2**: ON
   - **TLS**: ON（自動）
4. TunnelがDokployのNginxに接続されることを確認

**⚠️ 注意**: DokployのService設定ではポート80/443を公開しないでください。Cloudflare Tunnelが内部的にHTTP/HTTPSを処理します。

**注意**: 環境変数ファイル（.env）で以下の設定が正しくされていることを確認してください：
- `PLUGIN_DEBUGGING_HOST=0.0.0.0`
- `PLUGIN_REMOTE_INSTALLING_HOST=0.0.0.0`
- `PLUGIN_REMOTE_INSTALLING_PORT=5003`
- `PLUGIN_DIFY_INNER_API_URL=http://api:5001`

### 4. トラブルシューティング

**ポート80が既に割り当てられているエラーが発生した場合**:
- Cloudflare Tunnelを使用する場合は、DokployのPort設定でポート80/443を公開しない
- Docker ComposeのNginx設定で`ports`をコメントアウトし、`expose`のみ使用
- 外部ネットワーク `dokploy-network` が競合していないか確認

**404 Not Foundエラーが発生した場合**:
- Cloudflare TunnelのPublic Hostname設定を確認
- **Service**: `http://localhost:80` が正しく設定されているか確認
- Nginxコンテナが正常に起動しているか確認
- 内部ネットワーク通信が正常か確認

**Plugin Daemonエラーが発生した場合**:
- Plugin daemonのログを確認
- 環境変数 `PLUGIN_REMOTE_INSTALLING_HOST` が設定されていることを確認
- Plugin daemonコンテナが正常に起動していることを確認

**PostgreSQL認証エラーが発生した場合**:
- PostgreSQLコンテナが正常に起動していることを確認
- データベースの初期化が完了していることを確認
- 環境変数 `POSTGRES_PASSWORD` が正しく設定されていることを確認

**サービスが起動しない場合**:
- 各サービスのヘルスチェックが成功しているか確認
- 依存関係（db, redis）の起動順序を確認
- ログファイルでエラーを確認

### 5. デプロイ

1. **"Deploy Service"** をクリック
2. サービスが正常に起動するのを待つ
3. **各サービスのヘルスチェックが成功することを確認**:
   - Database: `Healthy`
   - Redis: `Started`
   - API: `Started`
   - Worker: `Started`
   - Web: `Started`
   - Nginx: `Started`
   - Plugin Daemon: `Started`
4. **Cloudflare Tunnelのステータスを確認**（別途設定が必要）

### 6. デプロイ後の確認

1. **コンテナログを確認**してエラーがないかチェック
2. **Nginxのヘルスチェック**: `http://localhost/health` で200応答を確認
3. **Cloudflare Tunnel経由で** `https://dify.hyper-typer.xyz` にアクセスして動作確認

### 7. 初期設定

1. ブラウザでコンソールURLにアクセス
2. 初期パスワードでログイン
3. 管理者パスワードを変更
4. 必要に応じて追加の設定

## トラブルシューティング

### 502 Bad Gateway エラー

502エラーが発生した場合の確認点：

1. **APIサービスの状態確認**:
   - APIコンテナが正常に起動しているか
   - ヘルスチェックが成功しているか

2. **Nginxの設定確認**:
   - アップストリーム設定が正しいか
   - タイムアウト設定が適切か

3. **ネットワーク接続確認**:
   - サービス間での通信が可能か
   - ポート設定が正しいか

4. **ログ確認**:
   - Nginxのエラーログを確認
   - APIサービスのログを確認
   - 各サービスのログをDokployで確認

### 一般的な問題と解決策

1. **データベース接続エラー**:
   - PostgreSQLのヘルスチェックが成功するまで待つ
   - データベースの接続設定を確認

2. **Redis接続エラー**:
   - Redisのパスワード設定を確認
   - Redisのヘルスチェックが成功することを確認

3. **ストレージエラー**:
   - ボリュームの権限を確認
   - ストレージディレクトリが正しくマウントされているか

4. **メモリ不足**:
   - 各サービスのメモリ制限を適切に設定
   - 必要に応じてリソースを増強

## サービス一覧

- **api**: Dify API サービス
- **worker**: Celeryワーカー
- **worker_beat**: スケジュールタスク
- **web**: フロントエンド
- **db**: PostgreSQLデータベース
- **redis**: Redisキャッシュ
- **sandbox**: コード実行サンドボックス
- **ssrf_proxy**: SSRFプロキシ
- **plugin_daemon**: プラグインデーモン
- **weaviate**: ベクターストア
- **nginx**: リバースプロキシ

## 推奨スペック

- **CPU**: 2コア以上
- **メモリ**: 4GB以上
- **ディスク**: 20GB以上
- **ネットワーク**: 100Mbps以上

## 監視

- 各サービスのヘルスチェックエンドポイントを定期的に監視
- ログの監視とアラート設定
- パフォーマンスメトリクスの監視

## バックアップ

- データベースの定期的なバックアップ
- 重要な設定ファイルのバックアップ
- ボリュームデータのバックアップ

## アップデート

1. 新しいバージョンのDifyイメージが利用可能な場合
2. docker-compose.dokploy.yaml を更新
3. middleware.env を更新
4. サービスを再デプロイ

## サポート

問題が発生した場合は：
1. ログを確認
2. 各サービスのヘルスチェックを確認
3. ネットワーク接続を確認
4. Dokployのサポートドキュメントを参照
5. Difyの公式ドキュメントを参照
