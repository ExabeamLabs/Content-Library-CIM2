# Code Changes for microsoft-evsecurity-xml-group-create-4754 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | time |  | ['({time}\d+-\d+-\d+T\d+:\d+:\d+\.\d+Z)', 'SystemTime=(\'|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)'] |