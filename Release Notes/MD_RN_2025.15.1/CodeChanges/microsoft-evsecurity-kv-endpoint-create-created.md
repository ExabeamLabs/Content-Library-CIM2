# Code Changes for microsoft-evsecurity-kv-endpoint-create-created (Parser)

| Code Change | Field Name | 2025.14.1 | 2025.15.1 |
|-------------|------------|-----------|------------|
| edit_regex_field | host | ['<Computer>({host}[\w\-.]+)</Computer>', '<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)'] | ['<Computer>({host}[\w\-.]+)<\/Computer>', '<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)'] |
| edit_regex_field | time | ['({time}\w+ \d+ \d+:\d+:\d+ \d\d\d\d)', "SystemTime='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"] | ['({time}\w+ \d+ \d+:\d+:\d+ \d\d\d\d)', 'SystemTime=(\'|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)'] |