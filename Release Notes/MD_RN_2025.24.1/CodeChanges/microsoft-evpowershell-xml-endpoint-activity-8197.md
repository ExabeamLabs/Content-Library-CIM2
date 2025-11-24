# Code Changes for microsoft-evpowershell-xml-endpoint-activity-8197 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | host |  | ['<Computer>({host}[\w.-]+)<\/Computer>', '<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)'] |