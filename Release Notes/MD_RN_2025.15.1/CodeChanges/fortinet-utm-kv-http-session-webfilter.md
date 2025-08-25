# Code Changes for fortinet-utm-kv-http-session-webfilter (Parser)

| Code Change | Field Name | 2025.14.1 | 2025.15.1 |
|-------------|------------|-----------|------------|
| edit_regex_field | url | ['\Wurl="({url}[^"]+)"'] | ['\Wurl="({url}[^"]+)"', 'url="({url}[^"]+)"'] |