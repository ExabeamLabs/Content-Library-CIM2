# Code Changes for microsoft-evapp-xml-endpoint-notification-success-1400 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | host |  | ['<Computer>({host}[\w.-]+)<\/Computer>', '<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)'] |