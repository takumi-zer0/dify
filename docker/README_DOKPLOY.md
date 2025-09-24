# Dify Dokploy Deployment Guide

このガイドでは、DifyをDokployでデプロイするための手順と設定について説明します。

## 前提条件

- Dokployがインストールされていること
- Dockerが利用可能な環境であること
- 十分なリソース（CPU、メモリ、ディスク容量）があること

## デプロイ手順

### 1. 環境設定

1. `docker/middleware.env.example` を `docker/middleware.env` にコピーします
2. 必要な環境変数を設定します：
   - `CONSOLE_API_URL`: コンソールAPIのURL（例: https://your-domain.com/console/api）
   - `CONSOLE_WEB_URL`: コンソールWebのURL（例: https://your-domain.com/console）
   - `APP_API_URL`: アプリケーションAPIのURL（例: https://your-domain.com/v1）
   - `APP_WEB_URL`: アプリケーションWebのURL（例: https://your-domain.com/app）
   - `SECRET_KEY`: 強力なシークレットキー（openssl rand -base64 42 で生成）
   - `INIT_PASSWORD`: 管理者パスワード
   - その他の必要な設定

### 2. Dokployでの設定

1. **Serviceの作成**:
   - Dokployのダッシュボードにアクセス
   - "Create Service" をクリック
   - Service Type: Docker Compose
   - Upload docker-compose.dokploy.yaml

2. **Environment Variables**:
   - middleware.env ファイルをアップロードまたは内容をコピー
   - 必要な環境変数を確認・修正

3. **Volumes**:
   - 必要なボリュームが自動的に作成されることを確認
   - データ永続化のためのボリューム設定

4. **Networking**:
   - 外部ネットワーク `dokploy-network` が存在することを確認
   - 必要に応じてネットワーク設定を調整

### 3. デプロイ

1. "Deploy Service" をクリック
2. サービスが正常に起動するのを待つ
3. 各サービスのヘルスチェックが成功することを確認

### 4. 初期設定

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
