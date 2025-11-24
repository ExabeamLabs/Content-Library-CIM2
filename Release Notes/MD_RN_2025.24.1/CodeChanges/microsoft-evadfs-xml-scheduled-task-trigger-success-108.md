# Code Changes for microsoft-evadfs-xml-scheduled-task-trigger-success-108 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | host |  | ['<Computer>({host}[\w.-]+)<\/Computer>', '<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)'] |