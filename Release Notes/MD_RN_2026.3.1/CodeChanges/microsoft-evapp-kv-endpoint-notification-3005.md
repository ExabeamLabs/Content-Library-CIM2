# Code Changes for microsoft-evapp-kv-endpoint-notification-3005 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | host |  | ['"Computer(Name)?":\s*"({host}[^"]+)"', '({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{6}[\+\-]\d{1,2}:\d{1,2})(\s({host}[\w\-.]+)\s)?', '({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)\s({host}\S+)\s({alert_severity}\S+)', '\s({host}[\w.-]+)\s+Web Event\s+Event code:\s*3005', 'exa_regex=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{6}[\+\-]\d{1,2}:\d{1,2})(\s({host}[\w\-.]+)\s)?', 'exa_regex=({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)\s({host}\S+)\s({alert_severity}\S+)', 'exa_regex=\s({host}[\w.-]+)\s+Web Event\s+Event code:\s*3005'] |