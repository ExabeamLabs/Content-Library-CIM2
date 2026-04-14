# Code Changes for postgresql-p-str-database-activity-detail (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | host |  | ['Z\s({host}\S+?)\spostgres\b', '\d\d:\d\d:\d\d ({host}[\w\-\.]+) [^:]+:\s+\[SecurityCenter\]:\s*'] |