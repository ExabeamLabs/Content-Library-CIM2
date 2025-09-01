# Code Changes for microsoft-evtaskscheduler-xml-scheduled-task-create-fail-104 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | user_sid |  | ['<Security UserID\\*=(\'|")({user_sid}[^\'<\/"]+)'] |