# Code Changes for claroty-ctd-cef-app-activity-success-catch-all (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | time |  | ['({time}\w\w\w \d\d \d\d\d\d \d\d:\d\d:\d\d)\s\w+\sCEF:', 'CtdTimeGenerated=({time}\w\w\w \d\d \d\d\d\d \d\d:\d\d:\d\d)', 'start=({time}\w\w\w \d\d \d\d\d\d \d\d:\d\d:\d\d)'] |