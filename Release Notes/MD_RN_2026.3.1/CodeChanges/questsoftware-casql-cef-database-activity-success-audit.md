# Code Changes for questsoftware-casql-cef-database-activity-success-audit (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_attribute | TimeFormat |  | yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ |
| edit_regex_field | time |  | ['({time}\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2}\.\d+(\+|-)\d+:\d+)'] |