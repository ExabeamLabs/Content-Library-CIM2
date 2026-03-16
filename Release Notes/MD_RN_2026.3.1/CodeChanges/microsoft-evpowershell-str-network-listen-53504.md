# Code Changes for microsoft-evpowershell-str-network-listen-53504 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | host |  | ['({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{6}[\+\-]\d{1,2}:\d{1,2})(\s({host}[\w\-.]+)\s)?', '\s({host}[\w.-]+)\s+PowerShell Named Pipe IPC\s+Windows PowerShell has started an IPC listening thread', '\w{3}\s\d\d\s\d\d:\d\d:\d\d\s({host}[^\s]+)\sMSWinEventLog'] |