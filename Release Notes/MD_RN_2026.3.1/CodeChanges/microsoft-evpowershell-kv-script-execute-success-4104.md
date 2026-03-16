# Code Changes for microsoft-evpowershell-kv-script-execute-success-4104 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | host |  | ['({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)((\.\d{6}[\+\-]\d{1,2}:\d{1,2})\s({host}[\w\-.]+)\s)?', 'ComputerName:\s*({host}[\w.-]+)', 'ComputerName=({host}({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[\w.\-]+))\s', '\s({host}[\w.-]+)\s+Execute a Remote Command\s+Creating Scriptblock text', '\w{3}\s\d\d\s\d\d:\d\d:\d\d\s({host}[^\s]+)\sMSWinEventLog'] |