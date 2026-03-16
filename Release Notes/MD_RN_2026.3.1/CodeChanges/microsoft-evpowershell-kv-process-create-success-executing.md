# Code Changes for microsoft-evpowershell-kv-process-create-success-executing (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | host |  | ['"(?:winlog\.)?computer_name"\s*:\s*"({dest_host}({host}[\w\-\.]+))', '<Computer>({dest_host}({host}[\w\-.]+))</Computer>', '<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)', 'ComputerName=({dest_host}({host}[\w.\-]+))', '\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{6}[\+\-]\d{1,2}:\d{1,2})\s({host}[\w\-.]+)\s', '\s+({host}[\w.-]+)\s+Executing Pipeline '] |