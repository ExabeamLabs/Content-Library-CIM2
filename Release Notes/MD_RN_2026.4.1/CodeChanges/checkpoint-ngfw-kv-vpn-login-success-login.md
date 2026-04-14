# Code Changes for checkpoint-ngfw-kv-vpn-login-success-login (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | time |  | ['\Wtime(:|=)"({time}\d{10})"', '\Wtime:"({time}\d{10})'] |