# Code Changes for microsoft-evsecurity-kv-ds-object-move-success-serviceobject (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | host |  | ['"Computer":"({host}[^"]+)', '\d\d:\d\d:\d\d\s+({host}({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({src_host}[\w.\-]+))\s+(Microsoft-Windows-Security-Auditing|MSWinEventLog)'] |