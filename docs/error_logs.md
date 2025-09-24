^^^^^^^^^^^^^^^^
File "/app/api/.venv/lib/python3.12/site-packages/click/core.py", line 1830, in invoke
return _process_result(sub_ctx.command.invoke(sub_ctx))
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
File "/app/api/.venv/lib/python3.12/site-packages/click/core.py", line 1226, in invoke
return ctx.invoke(self.callback, **ctx.params)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
File "/app/api/.venv/lib/python3.12/site-packages/click/core.py", line 794, in invoke
return callback(*args, **kwargs)
^^^^^^^^^^^^^^^^^^^^^^^^^
File "/app/api/commands.py", line 684, in upgrade_db
if lock.acquire(blocking=False):
^^^^^^^^^^^^^^^^^^^^^^^^^^^^
File "/app/api/.venv/lib/python3.12/site-packages/redis/lock.py", line 227, in acquire
if self.do_acquire(token):
^^^^^^^^^^^^^^^^^^^^^^
File "/app/api/.venv/lib/python3.12/site-packages/redis/lock.py", line 243, in do_acquire
if self.redis.set(self.name, token, nx=True, px=timeout):
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
File "/app/api/.venv/lib/python3.12/site-packages/redis/commands/core.py", line 2305, in set
return self.execute_command("SET", *pieces, **options)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
File "/app/api/.venv/lib/python3.12/site-packages/redis/client.py", line 624, in execute_command
return self._execute_command(*args, **options)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
File "/app/api/.venv/lib/python3.12/site-packages/redis/client.py", line 635, in _execute_command
return conn.retry.call_with_retry(
^^^^^^^^^^^^^^^^^^^^^^^^^^^
File "/app/api/.venv/lib/python3.12/site-packages/redis/retry.py", line 87, in call_with_retry
return do()
^^^^
File "/app/api/.venv/lib/python3.12/site-packages/redis/client.py", line 636, in <lambda>
lambda: self._send_command_parse_response(
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
File "/app/api/.venv/lib/python3.12/site-packages/redis/client.py", line 607, in _send_command_parse_response
return self.parse_response(conn, command_name, **options)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
File "/app/api/.venv/lib/python3.12/site-packages/redis/client.py", line 654, in parse_response
response = connection.read_response()
^^^^^^^^^^^^^^^^^^^^^^^^^^
File "/app/api/.venv/lib/python3.12/site-packages/redis/connection.py", line 666, in read_response
raise response
redis.exceptions.ResponseError: MISCONF Redis is configured to save RDB snapshots, but it is currently not able to persist on disk. Commands that may modify the data set are disabled, because this instance is configured to report errors during writes if RDB snapshotting fails (stop-writes-on-bgsave-error option). Please check the Redis logs for details about the RDB error.
Running migrations
/bin/bash: warning: setlocale: LC_ALL: cannot change locale (en_US.UTF-8)
/entrypoint.sh: line 7: warning: setlocale: LC_ALL: cannot change locale (en_US.UTF-8)
2025-09-24 06:36:19.234 INFO [MainThread] [utils.py:164] - NumExpr defaulting to 4 threads.
Preparing database migration...
Traceback (most recent call last):
File "/app/api/.venv/bin/flask", line 10, in <module>
sys.exit(main())
^^^^^^
File "/app/api/.venv/lib/python3.12/site-packages/flask/cli.py", line 1131, in main
cli.main()
File "/app/api/.venv/lib/python3.12/site-packages/click/core.py", line 1363, in main
rv = self.invoke(ctx)
^^^^^^^^^^^^^^^^
File "/app/api/.venv/lib/python3.12/site-packages/click/core.py", line 1830, in invoke
return _process_result(sub_ctx.command.invoke(sub_ctx))
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
File "/app/api/.venv/lib/python3.12/site-packages/click/core.py", line 1226, in invoke
return ctx.invoke(self.callback, **ctx.params)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
File "/app/api/.venv/lib/python3.12/site-packages/click/core.py", line 794, in invoke
return callback(*args, **kwargs)
^^^^^^^^^^^^^^^^^^^^^^^^^
File "/app/api/commands.py", line 684, in upgrade_db
if lock.acquire(blocking=False):
^^^^^^^^^^^^^^^^^^^^^^^^^^^^
File "/app/api/.venv/lib/python3.12/site-packages/redis/lock.py", line 227, in acquire
if self.do_acquire(token):
^^^^^^^^^^^^^^^^^^^^^^
File "/app/api/.venv/lib/python3.12/site-packages/redis/lock.py", line 243, in do_acquire
if self.redis.set(self.name, token, nx=True, px=timeout):
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
File "/app/api/.venv/lib/python3.12/site-packages/redis/commands/core.py", line 2305, in set
return self.execute_command("SET", *pieces, **options)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
File "/app/api/.venv/lib/python3.12/site-packages/redis/client.py", line 624, in execute_command
return self._execute_command(*args, **options)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
File "/app/api/.venv/lib/python3.12/site-packages/redis/client.py", line 635, in _execute_command
return conn.retry.call_with_retry(
^^^^^^^^^^^^^^^^^^^^^^^^^^^
File "/app/api/.venv/lib/python3.12/site-packages/redis/retry.py", line 87, in call_with_retry
return do()
^^^^
File "/app/api/.venv/lib/python3.12/site-packages/redis/client.py", line 636, in <lambda>
lambda: self._send_command_parse_response(
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
File "/app/api/.venv/lib/python3.12/site-packages/redis/client.py", line 607, in _send_command_parse_response
return self.parse_response(conn, command_name, **options)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
File "/app/api/.venv/lib/python3.12/site-packages/redis/client.py", line 654, in parse_response
response = connection.read_response()
^^^^^^^^^^^^^^^^^^^^^^^^^^
File "/app/api/.venv/lib/python3.12/site-packages/redis/connection.py", line 666, in read_response
raise response
redis.exceptions.ResponseError: MISCONF Redis is configured to save RDB snapshots, but it is currently not able to persist on disk. Commands that may modify the data set are disabled, because this instance is configured to report errors during writes if RDB snapshotting fails (stop-writes-on-bgsave-error option). Please check the Redis logs for details about the RDB error.

---

^^^^^^^^^^^^^^^^
File "/app/api/.venv/lib/python3.12/site-packages/click/core.py", line 1830, in invoke
return _process_result(sub_ctx.command.invoke(sub_ctx))
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
File "/app/api/.venv/lib/python3.12/site-packages/click/core.py", line 1226, in invoke
return ctx.invoke(self.callback, **ctx.params)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
File "/app/api/.venv/lib/python3.12/site-packages/click/core.py", line 794, in invoke
return callback(*args, **kwargs)
^^^^^^^^^^^^^^^^^^^^^^^^^
File "/app/api/commands.py", line 684, in upgrade_db
if lock.acquire(blocking=False):
^^^^^^^^^^^^^^^^^^^^^^^^^^^^
File "/app/api/.venv/lib/python3.12/site-packages/redis/lock.py", line 227, in acquire
if self.do_acquire(token):
^^^^^^^^^^^^^^^^^^^^^^
File "/app/api/.venv/lib/python3.12/site-packages/redis/lock.py", line 243, in do_acquire
if self.redis.set(self.name, token, nx=True, px=timeout):
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
File "/app/api/.venv/lib/python3.12/site-packages/redis/commands/core.py", line 2305, in set
return self.execute_command("SET", *pieces, **options)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
File "/app/api/.venv/lib/python3.12/site-packages/redis/client.py", line 624, in execute_command
return self._execute_command(*args, **options)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
File "/app/api/.venv/lib/python3.12/site-packages/redis/client.py", line 635, in _execute_command
return conn.retry.call_with_retry(
^^^^^^^^^^^^^^^^^^^^^^^^^^^
File "/app/api/.venv/lib/python3.12/site-packages/redis/retry.py", line 87, in call_with_retry
return do()
^^^^
File "/app/api/.venv/lib/python3.12/site-packages/redis/client.py", line 636, in <lambda>
lambda: self._send_command_parse_response(
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
File "/app/api/.venv/lib/python3.12/site-packages/redis/client.py", line 607, in _send_command_parse_response
return self.parse_response(conn, command_name, **options)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
File "/app/api/.venv/lib/python3.12/site-packages/redis/client.py", line 654, in parse_response
response = connection.read_response()
^^^^^^^^^^^^^^^^^^^^^^^^^^
File "/app/api/.venv/lib/python3.12/site-packages/redis/connection.py", line 666, in read_response
raise response
redis.exceptions.ResponseError: MISCONF Redis is configured to save RDB snapshots, but it is currently not able to persist on disk. Commands that may modify the data set are disabled, because this instance is configured to report errors during writes if RDB snapshotting fails (stop-writes-on-bgsave-error option). Please check the Redis logs for details about the RDB error.
/bin/bash: warning: setlocale: LC_ALL: cannot change locale (en_US.UTF-8)
/entrypoint.sh: line 7: warning: setlocale: LC_ALL: cannot change locale (en_US.UTF-8)
Running migrations
2025-09-24 06:36:28.379 INFO [MainThread] [utils.py:164] - NumExpr defaulting to 4 threads.
Preparing database migration...
Traceback (most recent call last):
File "/app/api/.venv/bin/flask", line 10, in <module>
sys.exit(main())
^^^^^^
File "/app/api/.venv/lib/python3.12/site-packages/flask/cli.py", line 1131, in main
cli.main()
File "/app/api/.venv/lib/python3.12/site-packages/click/core.py", line 1363, in main
rv = self.invoke(ctx)
^^^^^^^^^^^^^^^^
File "/app/api/.venv/lib/python3.12/site-packages/click/core.py", line 1830, in invoke
return _process_result(sub_ctx.command.invoke(sub_ctx))
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
File "/app/api/.venv/lib/python3.12/site-packages/click/core.py", line 1226, in invoke
return ctx.invoke(self.callback, **ctx.params)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
File "/app/api/.venv/lib/python3.12/site-packages/click/core.py", line 794, in invoke
return callback(*args, **kwargs)
^^^^^^^^^^^^^^^^^^^^^^^^^
File "/app/api/commands.py", line 684, in upgrade_db
if lock.acquire(blocking=False):
^^^^^^^^^^^^^^^^^^^^^^^^^^^^
File "/app/api/.venv/lib/python3.12/site-packages/redis/lock.py", line 227, in acquire
if self.do_acquire(token):
^^^^^^^^^^^^^^^^^^^^^^
File "/app/api/.venv/lib/python3.12/site-packages/redis/lock.py", line 243, in do_acquire
if self.redis.set(self.name, token, nx=True, px=timeout):
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
File "/app/api/.venv/lib/python3.12/site-packages/redis/commands/core.py", line 2305, in set
return self.execute_command("SET", *pieces, **options)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
File "/app/api/.venv/lib/python3.12/site-packages/redis/client.py", line 624, in execute_command
return self._execute_command(*args, **options)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
File "/app/api/.venv/lib/python3.12/site-packages/redis/client.py", line 635, in _execute_command
return conn.retry.call_with_retry(
^^^^^^^^^^^^^^^^^^^^^^^^^^^
File "/app/api/.venv/lib/python3.12/site-packages/redis/retry.py", line 87, in call_with_retry
return do()
^^^^
File "/app/api/.venv/lib/python3.12/site-packages/redis/client.py", line 636, in <lambda>
lambda: self._send_command_parse_response(
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
File "/app/api/.venv/lib/python3.12/site-packages/redis/client.py", line 607, in _send_command_parse_response
return self.parse_response(conn, command_name, **options)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
File "/app/api/.venv/lib/python3.12/site-packages/redis/client.py", line 654, in parse_response
response = connection.read_response()
^^^^^^^^^^^^^^^^^^^^^^^^^^
File "/app/api/.venv/lib/python3.12/site-packages/redis/connection.py", line 666, in read_response
raise response
redis.exceptions.ResponseError: MISCONF Redis is configured to save RDB snapshots, but it is currently not able to persist on disk. Commands that may modify the data set are disabled, because this instance is configured to report errors during writes if RDB snapshotting fails (stop-writes-on-bgsave-error option). Please check the Redis logs for details about the RDB error.

---

10.0.1.12 - - [24/Sep/2025:06:22:15 +0000] "GET /_next/static/chunks/6516-f9734f6965877053.js HTTP/1.1" 200 19834 "https://dify.hyper-typer.xyz/apps" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/140.0.0.0 Safari/537.36" "192.168.32.1"
10.0.1.12 - - [24/Sep/2025:06:22:15 +0000] "GET /_next/static/chunks/app/(commonLayout)/apps/page-e02d0d5f9a43ded1.js HTTP/1.1" 200 13849 "https://dify.hyper-typer.xyz/apps" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/140.0.0.0 Safari/537.36" "192.168.32.1"
10.0.1.12 - - [24/Sep/2025:06:22:15 +0000] "GET /_next/static/chunks/58663-a75025d4250ba1d7.js HTTP/1.1" 200 23844 "https://dify.hyper-typer.xyz/apps" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/140.0.0.0 Safari/537.36" "192.168.32.1"
10.0.1.12 - - [24/Sep/2025:06:22:15 +0000] "GET /_next/static/chunks/98611-3385436ac869beb4.js HTTP/1.1" 200 4065 "https://dify.hyper-typer.xyz/apps" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/140.0.0.0 Safari/537.36" "192.168.32.1"
10.0.1.12 - - [24/Sep/2025:06:22:15 +0000] "GET /_next/static/chunks/39997-af99ecf7a58c6e51.js HTTP/1.1" 200 2212 "https://dify.hyper-typer.xyz/apps" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/140.0.0.0 Safari/537.36" "192.168.32.1"
10.0.1.12 - - [24/Sep/2025:06:22:15 +0000] "GET /_next/static/chunks/91889-5a0ce10d39717b4f.js HTTP/1.1" 200 10413 "https://dify.hyper-typer.xyz/apps" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/140.0.0.0 Safari/537.36" "192.168.32.1"
10.0.1.12 - - [24/Sep/2025:06:22:15 +0000] "GET /_next/static/chunks/20570-0d1638281f87350b.js HTTP/1.1" 200 6932 "https://dify.hyper-typer.xyz/apps" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/140.0.0.0 Safari/537.36" "192.168.32.1"
10.0.1.12 - - [24/Sep/2025:06:22:15 +0000] "GET /_next/static/chunks/91713-61a7c60e549c3f9c.js HTTP/1.1" 200 5798 "https://dify.hyper-typer.xyz/apps" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/140.0.0.0 Safari/537.36" "192.168.32.1"
10.0.1.12 - - [24/Sep/2025:06:22:15 +0000] "GET /_next/static/css/82bcbd4b9b68d322.css HTTP/1.1" 200 30782 "https://dify.hyper-typer.xyz/apps" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/140.0.0.0 Safari/537.36" "192.168.32.1"
10.0.1.12 - - [24/Sep/2025:06:22:15 +0000] "GET /_next/static/css/43f3dbef98bdb566.css HTTP/1.1" 200 13257 "https://dify.hyper-typer.xyz/apps" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/140.0.0.0 Safari/537.36" "192.168.32.1"
10.0.1.12 - - [24/Sep/2025:06:22:15 +0000] "GET /_next/static/chunks/83334-ac179ef072c1e4ea.js HTTP/1.1" 200 13850 "https://dify.hyper-typer.xyz/apps" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/140.0.0.0 Safari/537.36" "192.168.32.1"
10.0.1.12 - - [24/Sep/2025:06:22:15 +0000] "GET /_next/static/chunks/59474-f425d56962df94c9.js HTTP/1.1" 200 32711 "https://dify.hyper-typer.xyz/apps" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/140.0.0.0 Safari/537.36" "192.168.32.1"
10.0.1.12 - - [24/Sep/2025:06:22:15 +0000] "GET /_next/static/chunks/59583-850396a0f34deb2b.js HTTP/1.1" 200 42531 "https://dify.hyper-typer.xyz/apps" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/140.0.0.0 Safari/537.36" "192.168.32.1"
10.0.1.12 - - [24/Sep/2025:06:22:15 +0000] "GET /_next/static/chunks/92969-c5c9edce1e2e6c8b.js HTTP/1.1" 200 6740 "https://dify.hyper-typer.xyz/apps" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/140.0.0.0 Safari/537.36" "192.168.32.1"
10.0.1.12 - - [24/Sep/2025:06:22:15 +0000] "GET /_next/static/chunks/11548-7f5f8aaaeea38516.js HTTP/1.1" 200 3845 "https://dify.hyper-typer.xyz/apps" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/140.0.0.0 Safari/537.36" "192.168.32.1"
10.0.1.12 - - [24/Sep/2025:06:22:15 +0000] "GET /_next/static/chunks/19971-f1cd7fb2335fa680.js HTTP/1.1" 200 12134 "https://dify.hyper-typer.xyz/apps" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/140.0.0.0 Safari/537.36" "192.168.32.1"
10.0.1.12 - - [24/Sep/2025:06:22:15 +0000] "GET /_next/static/chunks/bda40ab4-465678c6543fde64.js HTTP/1.1" 200 84324 "https://dify.hyper-typer.xyz/apps" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/140.0.0.0 Safari/537.36" "192.168.32.1"
10.0.1.12 - - [24/Sep/2025:06:22:15 +0000] "GET /_next/static/chunks/0b8e744a-4107c87d228bdc2c.js HTTP/1.1" 200 38151 "https://dify.hyper-typer.xyz/apps" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/140.0.0.0 Safari/537.36" "192.168.32.1"
10.0.1.12 - - [24/Sep/2025:06:22:15 +0000] "GET /_next/static/chunks/app/(commonLayout)/layout-43dcbdb931626b3d.js HTTP/1.1" 200 52737 "https://dify.hyper-typer.xyz/apps" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/140.0.0.0 Safari/537.36" "192.168.32.1"
10.0.1.12 - - [24/Sep/2025:06:22:15 +0000] "GET /_next/static/chunks/37047-36c3821d0e818f8a.js HTTP/1.1" 200 11652 "https://dify.hyper-typer.xyz/apps" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/140.0.0.0 Safari/537.36" "192.168.32.1"
10.0.1.12 - - [24/Sep/2025:06:22:15 +0000] "GET /_next/static/chunks/app/layout-c00836ec49a8fbe1.js HTTP/1.1" 200 5261 "https://dify.hyper-typer.xyz/apps" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/140.0.0.0 Safari/537.36" "192.168.32.1"
10.0.1.12 - - [24/Sep/2025:06:22:15 +0000] "GET /_next/static/chunks/42217-3333b08e7803809b.js HTTP/1.1" 200 7342 "https://dify.hyper-typer.xyz/apps" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/140.0.0.0 Safari/537.36" "192.168.32.1"
10.0.1.12 - - [24/Sep/2025:06:22:15 +0000] "GET /_next/static/chunks/83960-d769477c786aefef.js HTTP/1.1" 200 43614 "https://dify.hyper-typer.xyz/apps" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/140.0.0.0 Safari/537.36" "192.168.32.1"
10.0.1.12 - - [24/Sep/2025:06:22:15 +0000] "GET /_next/static/chunks/1668-584a3cb9e0cf70cd.js HTTP/1.1" 200 139406 "https://dify.hyper-typer.xyz/apps" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/140.0.0.0 Safari/537.36" "192.168.32.1"
10.0.1.12 - - [24/Sep/2025:06:22:16 +0000] "GET /_next/static/chunks/42530.3d6a9fb83aebc252.js HTTP/1.1" 200 3128 "https://dify.hyper-typer.xyz/apps" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/140.0.0.0 Safari/537.36" "192.168.32.1"
10.0.1.12 - - [24/Sep/2025:06:22:16 +0000] "GET /_next/static/chunks/76000.9d6c36a18d9cb51e.js HTTP/1.1" 200 1431 "https://dify.hyper-typer.xyz/apps" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/140.0.0.0 Safari/537.36" "192.168.32.1"
10.0.1.12 - - [24/Sep/2025:06:22:16 +0000] "GET /_next/static/chunks/58407.617fafc36fdde431.js HTTP/1.1" 200 2344 "https://dify.hyper-typer.xyz/apps" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/140.0.0.0 Safari/537.36" "192.168.32.1"
10.0.1.12 - - [24/Sep/2025:06:22:16 +0000] "GET /_next/static/chunks/55218.bbf7b8037aa79f47.js HTTP/1.1" 200 137 "https://dify.hyper-typer.xyz/apps" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/140.0.0.0 Safari/537.36" "192.168.32.1"
10.0.1.12 - - [24/Sep/2025:06:22:16 +0000] "GET /_next/static/chunks/81542.592c1648fe17c27f.js HTTP/1.1" 200 2792 "https://dify.hyper-typer.xyz/apps" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/140.0.0.0 Safari/537.36" "192.168.32.1"
10.0.1.12 - - [24/Sep/2025:06:22:16 +0000] "GET /_next/static/chunks/35025.54a788d7441bea9f.js HTTP/1.1" 200 5263 "https://dify.hyper-typer.xyz/apps" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/140.0.0.0 Safari/537.36" "192.168.32.1"
10.0.1.12 - - [24/Sep/2025:06:22:16 +0000] "GET /_next/static/chunks/58986.a2656e58b0456a1b.js HTTP/1.1" 200 724 "https://dify.hyper-typer.xyz/apps" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/140.0.0.0 Safari/537.36" "192.168.32.1"
10.0.1.12 - - [24/Sep/2025:06:22:16 +0000] "GET /_next/static/chunks/97298.cbd8f6b315070ac6.js HTTP/1.1" 200 5912 "https://dify.hyper-typer.xyz/apps" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/140.0.0.0 Safari/537.36" "192.168.32.1"
10.0.1.12 - - [24/Sep/2025:06:22:16 +0000] "GET /_next/static/chunks/53705.6882fd478ef7d544.js HTTP/1.1" 200 949 "https://dify.hyper-typer.xyz/apps" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/140.0.0.0 Safari/537.36" "192.168.32.1"
10.0.1.12 - - [24/Sep/2025:06:22:16 +0000] "GET /_next/static/chunks/28816.75b3b837205ada73.js HTTP/1.1" 200 8537 "https://dify.hyper-typer.xyz/apps" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/140.0.0.0 Safari/537.36" "192.168.32.1"
10.0.1.12 - - [24/Sep/2025:06:22:16 +0000] "GET /_next/static/chunks/85141.1718c6eb7b407405.js HTTP/1.1" 200 245 "https://dify.hyper-typer.xyz/apps" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/140.0.0.0 Safari/537.36" "192.168.32.1"
10.0.1.12 - - [24/Sep/2025:06:22:16 +0000] "GET /_next/static/chunks/61785.2425015034d24170.js HTTP/1.1" 200 1723 "https://dify.hyper-typer.xyz/apps" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/140.0.0.0 Safari/537.36" "192.168.32.1"
10.0.1.12 - - [24/Sep/2025:06:22:16 +0000] "GET /_next/static/chunks/12125.edfd15617c84877a.js HTTP/1.1" 200 1461 "https://dify.hyper-typer.xyz/apps" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/140.0.0.0 Safari/537.36" "192.168.32.1"
10.0.1.12 - - [24/Sep/2025:06:22:16 +0000] "GET /_next/static/chunks/45318.137535f1d15c8f8b.js HTTP/1.1" 200 3567 "https://dify.hyper-typer.xyz/apps" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/140.0.0.0 Safari/537.36" "192.168.32.1"
10.0.1.12 - - [24/Sep/2025:06:22:16 +0000] "GET /_next/static/chunks/19326.0b82f45c328b4182.js HTTP/1.1" 200 10847 "https://dify.hyper-typer.xyz/apps" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/140.0.0.0 Safari/537.36" "192.168.32.1"
10.0.1.12 - - [24/Sep/2025:06:22:16 +0000] "GET /_next/static/chunks/40356.437355e9e3e89f89.js HTTP/1.1" 200 657 "https://dify.hyper-typer.xyz/apps" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/140.0.0.0 Safari/537.36" "192.168.32.1"
10.0.1.12 - - [24/Sep/2025:06:22:16 +0000] "GET /_next/static/chunks/16711.4200241536dea973.js HTTP/1.1" 200 836 "https://dify.hyper-typer.xyz/apps" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/140.0.0.0 Safari/537.36" "192.168.32.1"
10.0.1.12 - - [24/Sep/2025:06:22:16 +0000] "GET /_next/static/chunks/68678.fd7e2763150e6bf0.js HTTP/1.1" 200 4987 "https://dify.hyper-typer.xyz/apps" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/140.0.0.0 Safari/537.36" "192.168.32.1"
10.0.1.12 - - [24/Sep/2025:06:22:16 +0000] "GET /_next/static/chunks/30606.50f22966336153cc.js HTTP/1.1" 200 571 "https://dify.hyper-typer.xyz/apps" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/140.0.0.0 Safari/537.36" "192.168.32.1"
10.0.1.12 - - [24/Sep/2025:06:22:16 +0000] "GET /_next/static/chunks/68238.e942ac8bfc1a500c.js HTTP/1.1" 200 3768 "https://dify.hyper-typer.xyz/apps" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/140.0.0.0 Safari/537.36" "192.168.32.1"
10.0.1.12 - - [24/Sep/2025:06:22:16 +0000] "GET /_next/static/chunks/58854.cccd3dda7f227bbb.js HTTP/1.1" 200 1445 "https://dify.hyper-typer.xyz/apps" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/140.0.0.0 Safari/537.36" "192.168.32.1"
10.0.1.12 - - [24/Sep/2025:06:22:16 +0000] "GET /_next/static/chunks/93797.46340eb968a7474e.js HTTP/1.1" 200 4225 "https://dify.hyper-typer.xyz/apps" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/140.0.0.0 Safari/537.36" "192.168.32.1"
10.0.1.12 - - [24/Sep/2025:06:22:16 +0000] "GET /_next/static/chunks/34831.2b6e51f7ad0f1795.js HTTP/1.1" 200 1760 "https://dify.hyper-typer.xyz/apps" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/140.0.0.0 Safari/537.36" "192.168.32.1"
10.0.1.12 - - [24/Sep/2025:06:22:16 +0000] "GET /_next/static/chunks/42054.a89c82b1a3fa50df.js HTTP/1.1" 200 799 "https://dify.hyper-typer.xyz/apps" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/140.0.0.0 Safari/537.36" "192.168.32.1"
10.0.1.12 - - [24/Sep/2025:06:22:16 +0000] "GET /_next/static/chunks/85956.a742f2466e4015a3.js HTTP/1.1" 200 2566 "https://dify.hyper-typer.xyz/apps" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/140.0.0.0 Safari/537.36" "192.168.32.1"
10.0.1.12 - - [24/Sep/2025:06:22:16 +0000] "GET /_next/static/chunks/49324.118397f73d9533a4.js HTTP/1.1" 200 4535 "https://dify.hyper-typer.xyz/apps" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/140.0.0.0 Safari/537.36" "192.168.32.1"
10.0.1.12 - - [24/Sep/2025:06:22:16 +0000] "GET /_next/static/chunks/61068.6c10151d2f552ed6.js HTTP/1.1" 200 732 "https://dify.hyper-typer.xyz/apps" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/140.0.0.0 Safari/537.36" "192.168.32.1"
10.0.1.12 - - [24/Sep/2025:06:22:16 +0000] "GET /_next/static/chunks/8094.27df35d51034f739.js HTTP/1.1" 200 712 "https://dify.hyper-typer.xyz/apps" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/140.0.0.0 Safari/537.36" "192.168.32.1"
10.0.1.12 - - [24/Sep/2025:06:22:16 +0000] "GET /_next/static/chunks/15606.74e812dfbc40c8ec.js HTTP/1.1" 200 13045 "https://dify.hyper-typer.xyz/apps" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/140.0.0.0 Safari/537.36" "192.168.32.1"
10.0.1.12 - - [24/Sep/2025:06:22:16 +0000] "GET /icon-192x192.png HTTP/1.1" 200 3464 "https://dify.hyper-typer.xyz/apps" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/140.0.0.0 Safari/537.36" "192.168.32.1"
10.0.1.12 - - [24/Sep/2025:06:22:16 +0000] "GET /manifest.json HTTP/1.1" 200 470 "https://dify.hyper-typer.xyz/apps" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/140.0.0.0 Safari/537.36" "192.168.32.1"
2025/09/24 06:22:19 [error] 21#21: *98 connect() failed (113: No route to host) while connecting to upstream, client: 10.0.1.12, server: dify.hyper-typer.xyz, request: "GET /console/api/system-features HTTP/1.1", upstream: "http://192.168.64.9:5001/console/api/system-features", host: "dify.hyper-typer.xyz", referrer: "https://dify.hyper-typer.xyz/apps"
10.0.1.12 - - [24/Sep/2025:06:22:19 +0000] "GET /console/api/system-features HTTP/1.1" 502 559 "https://dify.hyper-typer.xyz/apps" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/140.0.0.0 Safari/537.36" "192.168.32.1"
2025/09/24 06:22:22 [error] 21#21: *98 connect() failed (113: No route to host) while connecting to upstream, client: 10.0.1.12, server: dify.hyper-typer.xyz, request: "GET /console/api/setup HTTP/1.1", upstream: "http://192.168.64.9:5001/console/api/setup", host: "dify.hyper-typer.xyz", referrer: "https://dify.hyper-typer.xyz/apps"
10.0.1.12 - - [24/Sep/2025:06:22:22 +0000] "GET /console/api/setup HTTP/1.1" 502 559 "https://dify.hyper-typer.xyz/apps" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/140.0.0.0 Safari/537.36" "192.168.32.1"
10.0.1.12 - - [24/Sep/2025:06:22:22 +0000] "GET /install?_rsc=15dbi HTTP/1.1" 200 1228 "https://dify.hyper-typer.xyz/apps" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/140.0.0.0 Safari/537.36" "192.168.32.1"
10.0.1.12 - - [24/Sep/2025:06:22:22 +0000] "GET /_next/static/chunks/83318-b1c6b59111ab16d4.js HTTP/1.1" 200 8521 "https://dify.hyper-typer.xyz/apps" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/140.0.0.0 Safari/537.36" "192.168.32.1"
10.0.1.12 - - [24/Sep/2025:06:22:22 +0000] "GET /_next/static/chunks/5878-1ed185cb0275028d.js HTTP/1.1" 200 14359 "https://dify.hyper-typer.xyz/apps" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/140.0.0.0 Safari/537.36" "192.168.32.1"
10.0.1.12 - - [24/Sep/2025:06:22:22 +0000] "GET /_next/static/chunks/51206-c0901ef971679f6d.js HTTP/1.1" 200 12943 "https://dify.hyper-typer.xyz/apps" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/140.0.0.0 Safari/537.36" "192.168.32.1"
10.0.1.12 - - [24/Sep/2025:06:22:22 +0000] "GET /_next/static/chunks/app/install/page-6f8bab0af4203c4f.js HTTP/1.1" 200 2103 "https://dify.hyper-typer.xyz/apps" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/140.0.0.0 Safari/537.36" "192.168.32.1"
10.0.1.12 - - [24/Sep/2025:06:22:22 +0000] "GET /_next/static/chunks/43772-7fc0f642bc11e7af.js HTTP/1.1" 200 7808 "https://dify.hyper-typer.xyz/apps" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/140.0.0.0 Safari/537.36" "192.168.32.1"
10.0.1.12 - - [24/Sep/2025:06:22:22 +0000] "GET /_next/static/chunks/1898.89ba096be8637f07.js HTTP/1.1" 200 1865 "https://dify.hyper-typer.xyz/apps" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/140.0.0.0 Safari/537.36" "192.168.32.1"
10.0.1.12 - - [24/Sep/2025:06:22:22 +0000] "GET /_next/static/chunks/37267.a7e4a4613224ab8b.js HTTP/1.1" 200 3098 "https://dify.hyper-typer.xyz/apps" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/140.0.0.0 Safari/537.36" "192.168.32.1"
10.0.1.12 - - [24/Sep/2025:06:22:22 +0000] "GET /favicon.ico HTTP/1.1" 200 976 "https://dify.hyper-typer.xyz/install" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/140.0.0.0 Safari/537.36" "192.168.32.1"
10.0.1.12 - - [24/Sep/2025:06:22:22 +0000] "GET /logo/logo-monochrome-white.svg HTTP/1.1" 200 583 "https://dify.hyper-typer.xyz/install" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/140.0.0.0 Safari/537.36" "192.168.32.1"
2025/09/24 06:22:25 [error] 21#21: *98 connect() failed (113: No route to host) while connecting to upstream, client: 10.0.1.12, server: dify.hyper-typer.xyz, request: "GET /console/api/setup HTTP/1.1", upstream: "http://192.168.64.9:5001/console/api/setup", host: "dify.hyper-typer.xyz", referrer: "https://dify.hyper-typer.xyz/install"
10.0.1.12 - - [24/Sep/2025:06:22:25 +0000] "GET /console/api/setup HTTP/1.1" 502 559 "https://dify.hyper-typer.xyz/install" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/140.0.0.0 Safari/537.36" "192.168.32.1"
2025/09/24 06:22:30 [error] 21#21: *98 connect() failed (113: No route to host) while connecting to upstream, client: 10.0.1.12, server: dify.hyper-typer.xyz, request: "GET /console/api/system-features HTTP/1.1", upstream: "http://192.168.64.9:5001/console/api/system-features", host: "dify.hyper-typer.xyz", referrer: "https://dify.hyper-typer.xyz/install"
10.0.1.12 - - [24/Sep/2025:06:22:30 +0000] "GET /console/api/system-features HTTP/1.1" 502 559 "https://dify.hyper-typer.xyz/install" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/140.0.0.0 Safari/537.36" "192.168.32.1"
10.0.1.12 - - [24/Sep/2025:06:22:43 +0000] "GET /console/api/system-features HTTP/1.1" 502 559 "https://dify.hyper-typer.xyz/install" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/140.0.0.0 Safari/537.36" "192.168.32.1"
2025/09/24 06:22:43 [error] 21#21: *98 connect() failed (113: No route to host) while connecting to upstream, client: 10.0.1.12, server: dify.hyper-typer.xyz, request: "GET /console/api/system-features HTTP/1.1", upstream: "http://192.168.64.9:5001/console/api/system-features", host: "dify.hyper-typer.xyz", referrer: "https://dify.hyper-typer.xyz/install"
2025/09/24 06:22:50 [error] 21#21: *98 connect() failed (113: No route to host) while connecting to upstream, client: 10.0.1.12, server: dify.hyper-typer.xyz, request: "GET /console/api/system-features HTTP/1.1", upstream: "http://192.168.64.9:5001/console/api/system-features", host: "dify.hyper-typer.xyz", referrer: "https://dify.hyper-typer.xyz/install"
10.0.1.12 - - [24/Sep/2025:06:22:50 +0000] "GET /console/api/system-features HTTP/1.1" 502 559 "https://dify.hyper-typer.xyz/install" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/140.0.0.0 Safari/537.36" "192.168.32.1"
2025/09/24 06:22:53 [error] 21#21: *98 connect() failed (113: No route to host) while connecting to upstream, client: 10.0.1.12, server: dify.hyper-typer.xyz, request: "GET /console/api/setup HTTP/1.1", upstream: "http://192.168.64.9:5001/console/api/setup", host: "dify.hyper-typer.xyz", referrer: "https://dify.hyper-typer.xyz/install"
10.0.1.12 - - [24/Sep/2025:06:22:53 +0000] "GET /console/api/setup HTTP/1.1" 502 559 "https://dify.hyper-typer.xyz/install" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/140.0.0.0 Safari/537.36" "192.168.32.1"
10.0.1.12 - - [24/Sep/2025:06:30:46 +0000] "GET / HTTP/1.1" 307 15 "-" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/140.0.0.0 Safari/537.36" "192.168.32.1"
10.0.1.12 - - [24/Sep/2025:06:30:46 +0000] "GET /apps HTTP/1.1" 200 13060 "-" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/140.0.0.0 Safari/537.36" "192.168.32.1"
2025/09/24 06:30:46 [error] 21#21: *152 connect() failed (113: No route to host) while connecting to upstream, client: 10.0.1.12, server: dify.hyper-typer.xyz, request: "GET /console/api/system-features HTTP/1.1", upstream: "http://192.168.64.9:5001/console/api/system-features", host: "dify.hyper-typer.xyz", referrer: "https://dify.hyper-typer.xyz/install"
10.0.1.12 - - [24/Sep/2025:06:30:46 +0000] "GET /console/api/system-features HTTP/1.1" 502 559 "https://dify.hyper-typer.xyz/install" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/140.0.0.0 Safari/537.36" "192.168.32.1"
10.0.1.12 - - [24/Sep/2025:06:30:46 +0000] "GET /manifest.json HTTP/1.1" 304 0 "https://dify.hyper-typer.xyz/apps" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/140.0.0.0 Safari/537.36" "192.168.32.1"
10.0.1.12 - - [24/Sep/2025:06:30:49 +0000] "GET /console/api/system-features HTTP/1.1" 502 559 "https://dify.hyper-typer.xyz/apps" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/140.0.0.0 Safari/537.36" "192.168.32.1"
2025/09/24 06:30:49 [error] 21#21: *152 connect() failed (113: No route to host) while connecting to upstream, client: 10.0.1.12, server: dify.hyper-typer.xyz, request: "GET /console/api/system-features HTTP/1.1", upstream: "http://192.168.64.9:5001/console/api/system-features", host: "dify.hyper-typer.xyz", referrer: "https://dify.hyper-typer.xyz/apps"
2025/09/24 06:30:52 [error] 21#21: *152 connect() failed (113: No route to host) while connecting to upstream, client: 10.0.1.12, server: dify.hyper-typer.xyz, request: "GET /console/api/setup HTTP/1.1", upstream: "http://192.168.64.9:5001/console/api/setup", host: "dify.hyper-typer.xyz", referrer: "https://dify.hyper-typer.xyz/apps"
10.0.1.12 - - [24/Sep/2025:06:30:52 +0000] "GET /console/api/setup HTTP/1.1" 502 559 "https://dify.hyper-typer.xyz/apps" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/140.0.0.0 Safari/537.36" "192.168.32.1"
10.0.1.12 - - [24/Sep/2025:06:30:52 +0000] "GET /install?_rsc=15dbi HTTP/1.1" 200 1229 "https://dify.hyper-typer.xyz/apps" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/140.0.0.0 Safari/537.36" "192.168.32.1"
10.0.1.12 - - [24/Sep/2025:06:30:55 +0000] "GET /console/api/setup HTTP/1.1" 502 559 "https://dify.hyper-typer.xyz/install" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/140.0.0.0 Safari/537.36" "192.168.32.1"
2025/09/24 06:30:55 [error] 21#21: *152 connect() failed (113: No route to host) while connecting to upstream, client: 10.0.1.12, server: dify.hyper-typer.xyz, request: "GET /console/api/setup HTTP/1.1", upstream: "http://192.168.64.9:5001/console/api/setup", host: "dify.hyper-typer.xyz", referrer: "https://dify.hyper-typer.xyz/install"
10.0.1.12 - - [24/Sep/2025:06:36:48 +0000] "GET /install HTTP/1.1" 200 6461 "-" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/140.0.0.0 Safari/537.36" "192.168.32.1"
10.0.1.12 - - [24/Sep/2025:06:36:48 +0000] "GET /icon-192x192.png HTTP/1.1" 200 3464 "https://dify.hyper-typer.xyz/install" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/140.0.0.0 Safari/537.36" "192.168.32.1"
10.0.1.12 - - [24/Sep/2025:06:36:48 +0000] "GET /manifest.json HTTP/1.1" 304 0 "https://dify.hyper-typer.xyz/install" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/140.0.0.0 Safari/537.36" "192.168.32.1"
2025/09/24 06:36:51 [error] 21#21: *162 connect() failed (113: No route to host) while connecting to upstream, client: 10.0.1.12, server: dify.hyper-typer.xyz, request: "GET /console/api/system-features HTTP/1.1", upstream: "http://192.168.64.9:5001/console/api/system-features", host: "dify.hyper-typer.xyz", referrer: "https://dify.hyper-typer.xyz/install"
10.0.1.12 - - [24/Sep/2025:06:36:51 +0000] "GET /console/api/system-features HTTP/1.1" 502 559 "https://dify.hyper-typer.xyz/install" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/140.0.0.0 Safari/537.36" "192.168.32.1"
10.0.1.12 - - [24/Sep/2025:06:36:51 +0000] "GET /favicon.ico HTTP/1.1" 200 976 "https://dify.hyper-typer.xyz/install" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/140.0.0.0 Safari/537.36" "192.168.32.1"
2025/09/24 06:36:54 [error] 21#21: *162 connect() failed (113: No route to host) while connecting to upstream, client: 10.0.1.12, server: dify.hyper-typer.xyz, request: "GET /console/api/setup HTTP/1.1", upstream: "http://192.168.64.9:5001/console/api/setup", host: "dify.hyper-typer.xyz", referrer: "https://dify.hyper-typer.xyz/install"
10.0.1.12 - - [24/Sep/2025:06:36:54 +0000] "GET /console/api/setup HTTP/1.1" 502 559 "https://dify.hyper-typer.xyz/install" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/140.0.0.0 Safari/537.36" "192.168.32.1"

---

/bin/bash: warning: setlocale: LC_ALL: cannot change locale (en_US.UTF-8)
bash: warning: setlocale: LC_ALL: cannot change locale (en_US.UTF-8)
2025/09/24 06:33:37 pool.go:32: [INFO]init routine pool, size: 10000
2025/09/24 06:33:38 init.go:104: [INFO]dify plugin db initialized
2025/09/24 06:33:38 manager.go:114: [INFO]start plugin manager daemon...
2025/09/24 06:33:38 manager.go:141: [PANIC]init redis client failed: MISCONF Redis is configured to save RDB snapshots, but it is currently not able to persist on disk. Commands that may modify the data set are disabled, because this instance is configured to report errors during writes if RDB snapshotting fails (stop-writes-on-bgsave-error option). Please check the Redis logs for details about the RDB error.
panic: [PANIC]init redis client failed: MISCONF Redis is configured to save RDB snapshots, but it is currently not able to persist on disk. Commands that may modify the data set are disabled, because this instance is configured to report errors during writes if RDB snapshotting fails (stop-writes-on-bgsave-error option). Please check the Redis logs for details about the RDB error.
goroutine 1 [running]:
github.com/langgenius/dify-plugin-daemon/internal/utils/log.writeLog({0x26930ca, 0x5}, {0x26cc78c?, 0x0?}, 0x1, {0xc000123cc0, 0x1, 0x1})
/app/internal/utils/log/log.go:40 +0x305
github.com/langgenius/dify-plugin-daemon/internal/utils/log.Panic(...)
/app/internal/utils/log/log.go:66
github.com/langgenius/dify-plugin-daemon/internal/core/plugin_manager.(*PluginManager).Launch(0xc0006c6bb0, 0xc0005a4688)
/app/internal/core/plugin_manager/manager.go:141 +0x2ef
github.com/langgenius/dify-plugin-daemon/internal/server.(*App).Run(0xc000010ed0, 0xc0005a4688)
/app/internal/server/server.go:108 +0x197
main.main()
/app/cmd/server/main.go:28 +0x125
/bin/bash: warning: setlocale: LC_ALL: cannot change locale (en_US.UTF-8)
/bin/bash: warning: setlocale: LC_ALL: cannot change locale (en_US.UTF-8)
bash: warning: setlocale: LC_ALL: cannot change locale (en_US.UTF-8)
2025/09/24 06:34:38 pool.go:32: [INFO]init routine pool, size: 10000
2025/09/24 06:34:39 init.go:104: [INFO]dify plugin db initialized
2025/09/24 06:34:39 manager.go:114: [INFO]start plugin manager daemon...
2025/09/24 06:34:39 manager.go:141: [PANIC]init redis client failed: MISCONF Redis is configured to save RDB snapshots, but it is currently not able to persist on disk. Commands that may modify the data set are disabled, because this instance is configured to report errors during writes if RDB snapshotting fails (stop-writes-on-bgsave-error option). Please check the Redis logs for details about the RDB error.
panic: [PANIC]init redis client failed: MISCONF Redis is configured to save RDB snapshots, but it is currently not able to persist on disk. Commands that may modify the data set are disabled, because this instance is configured to report errors during writes if RDB snapshotting fails (stop-writes-on-bgsave-error option). Please check the Redis logs for details about the RDB error.
goroutine 1 [running]:
github.com/langgenius/dify-plugin-daemon/internal/utils/log.writeLog({0x26930ca, 0x5}, {0x26cc78c?, 0x0?}, 0x1, {0xc000593cc0, 0x1, 0x1})
/app/internal/utils/log/log.go:40 +0x305
github.com/langgenius/dify-plugin-daemon/internal/utils/log.Panic(...)
/app/internal/utils/log/log.go:66
github.com/langgenius/dify-plugin-daemon/internal/core/plugin_manager.(*PluginManager).Launch(0xc000710160, 0xc0005f2588)
/app/internal/core/plugin_manager/manager.go:141 +0x2ef
github.com/langgenius/dify-plugin-daemon/internal/server.(*App).Run(0xc000513050, 0xc0005f2588)
/app/internal/server/server.go:108 +0x197
main.main()
/app/cmd/server/main.go:28 +0x125
/bin/bash: warning: setlocale: LC_ALL: cannot change locale (en_US.UTF-8)
/bin/bash: warning: setlocale: LC_ALL: cannot change locale (en_US.UTF-8)
bash: warning: setlocale: LC_ALL: cannot change locale (en_US.UTF-8)
2025/09/24 06:35:39 pool.go:32: [INFO]init routine pool, size: 10000
2025/09/24 06:35:40 init.go:104: [INFO]dify plugin db initialized
2025/09/24 06:35:40 manager.go:114: [INFO]start plugin manager daemon...
2025/09/24 06:35:40 manager.go:141: [PANIC]init redis client failed: MISCONF Redis is configured to save RDB snapshots, but it is currently not able to persist on disk. Commands that may modify the data set are disabled, because this instance is configured to report errors during writes if RDB snapshotting fails (stop-writes-on-bgsave-error option). Please check the Redis logs for details about the RDB error.
panic: [PANIC]init redis client failed: MISCONF Redis is configured to save RDB snapshots, but it is currently not able to persist on disk. Commands that may modify the data set are disabled, because this instance is configured to report errors during writes if RDB snapshotting fails (stop-writes-on-bgsave-error option). Please check the Redis logs for details about the RDB error.
goroutine 1 [running]:
github.com/langgenius/dify-plugin-daemon/internal/utils/log.writeLog({0x26930ca, 0x5}, {0x26cc78c?, 0x0?}, 0x1, {0xc000155cc0, 0x1, 0x1})
/app/internal/utils/log/log.go:40 +0x305
github.com/langgenius/dify-plugin-daemon/internal/utils/log.Panic(...)
/app/internal/utils/log/log.go:66
github.com/langgenius/dify-plugin-daemon/internal/core/plugin_manager.(*PluginManager).Launch(0xc0006160b0, 0xc000552b08)
/app/internal/core/plugin_manager/manager.go:141 +0x2ef
github.com/langgenius/dify-plugin-daemon/internal/server.(*App).Run(0xc00011b080, 0xc000552b08)
/app/internal/server/server.go:108 +0x197
main.main()
/app/cmd/server/main.go:28 +0x125
/bin/bash: warning: setlocale: LC_ALL: cannot change locale (en_US.UTF-8)
/bin/bash: warning: setlocale: LC_ALL: cannot change locale (en_US.UTF-8)
bash: warning: setlocale: LC_ALL: cannot change locale (en_US.UTF-8)
2025/09/24 06:36:40 pool.go:32: [INFO]init routine pool, size: 10000
2025/09/24 06:36:40 init.go:104: [INFO]dify plugin db initialized
2025/09/24 06:36:40 manager.go:114: [INFO]start plugin manager daemon...
2025/09/24 06:36:40 manager.go:141: [PANIC]init redis client failed: MISCONF Redis is configured to save RDB snapshots, but it is currently not able to persist on disk. Commands that may modify the data set are disabled, because this instance is configured to report errors during writes if RDB snapshotting fails (stop-writes-on-bgsave-error option). Please check the Redis logs for details about the RDB error.
panic: [PANIC]init redis client failed: MISCONF Redis is configured to save RDB snapshots, but it is currently not able to persist on disk. Commands that may modify the data set are disabled, because this instance is configured to report errors during writes if RDB snapshotting fails (stop-writes-on-bgsave-error option). Please check the Redis logs for details about the RDB error.
goroutine 1 [running]:
github.com/langgenius/dify-plugin-daemon/internal/utils/log.writeLog({0x26930ca, 0x5}, {0x26cc78c?, 0x0?}, 0x1, {0xc000587cc0, 0x1, 0x1})
/app/internal/utils/log/log.go:40 +0x305
github.com/langgenius/dify-plugin-daemon/internal/utils/log.Panic(...)
/app/internal/utils/log/log.go:66
github.com/langgenius/dify-plugin-daemon/internal/core/plugin_manager.(*PluginManager).Launch(0xc0005b6b00, 0xc000144008)
/app/internal/core/plugin_manager/manager.go:141 +0x2ef
github.com/langgenius/dify-plugin-daemon/internal/server.(*App).Run(0xc0001a6090, 0xc000144008)
/app/internal/server/server.go:108 +0x197
main.main()
/app/cmd/server/main.go:28 +0x125
/bin/bash: warning: setlocale: LC_ALL: cannot change locale (en_US.UTF-8)
/bin/bash: warning: setlocale: LC_ALL: cannot change locale (en_US.UTF-8)
bash: warning: setlocale: LC_ALL: cannot change locale (en_US.UTF-8)
2025/09/24 06:37:41 pool.go:32: [INFO]init routine pool, size: 10000
2025/09/24 06:37:41 init.go:104: [INFO]dify plugin db initialized
2025/09/24 06:37:41 manager.go:114: [INFO]start plugin manager daemon...
2025/09/24 06:37:41 manager.go:141: [PANIC]init redis client failed: MISCONF Redis is configured to save RDB snapshots, but it is currently not able to persist on disk. Commands that may modify the data set are disabled, because this instance is configured to report errors during writes if RDB snapshotting fails (stop-writes-on-bgsave-error option). Please check the Redis logs for details about the RDB error.
panic: [PANIC]init redis client failed: MISCONF Redis is configured to save RDB snapshots, but it is currently not able to persist on disk. Commands that may modify the data set are disabled, because this instance is configured to report errors during writes if RDB snapshotting fails (stop-writes-on-bgsave-error option). Please check the Redis logs for details about the RDB error.
goroutine 1 [running]:
github.com/langgenius/dify-plugin-daemon/internal/utils/log.writeLog({0x26930ca, 0x5}, {0x26cc78c?, 0x0?}, 0x1, {0xc000659cc0, 0x1, 0x1})
/app/internal/utils/log/log.go:40 +0x305
github.com/langgenius/dify-plugin-daemon/internal/utils/log.Panic(...)
/app/internal/utils/log/log.go:66
github.com/langgenius/dify-plugin-daemon/internal/core/plugin_manager.(*PluginManager).Launch(0xc00063ab00, 0xc00056cb08)
/app/internal/core/plugin_manager/manager.go:141 +0x2ef
github.com/langgenius/dify-plugin-daemon/internal/server.(*App).Run(0xc00011b230, 0xc00056cb08)
/app/internal/server/server.go:108 +0x197
main.main()
/app/cmd/server/main.go:28 +0x125