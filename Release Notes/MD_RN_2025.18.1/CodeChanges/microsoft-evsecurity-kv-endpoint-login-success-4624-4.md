# Code Changes for microsoft-evsecurity-kv-endpoint-login-success-4624-4 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | auth_package |  | ['ログオン プロセス:\s+({auth_process}[^\s]+)\s+認証パッケージ:\s+({auth_package}[^\s]+)', '移行されたサービス:\s+-\s+パッケージ名\s+\(NTLM\s+のみ\):\s+({auth_package}.+?)\s+キーの長さ'] |