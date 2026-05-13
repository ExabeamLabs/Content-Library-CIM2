# Code Changes for microsoft-windows-kv-endpoint-logout-success-23 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | channel |  | ['"Channel"+:"+({channel}[^"]+)"', 'channel="({channel}[^"]+)', 'exa_regex="Channel"+:"+({channel}[^"]+)"'] |