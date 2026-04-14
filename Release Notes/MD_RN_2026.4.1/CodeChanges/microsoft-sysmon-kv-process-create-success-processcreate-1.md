# Code Changes for microsoft-sysmon-kv-process-create-success-processcreate-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | host |  | ['<Computer>({src_host}({host}[^<]+?))</Computer>', '\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{6}[\+\-]\d{1,2}:\d{1,2})\s({host}[\w\-.]+)\s', '\sComputer="({src_host}({host}[\w\-.]+))"'] |
| edit_regex_field | src_host |  | ['<Computer>({src_host}({host}[^<]+?))</Computer>', '\sComputer="({src_host}({host}[\w\-.]+))"'] |
| edit_regex_field | user_sid |  | [' Sid=\s*({user_sid}[^\s]+)'] |