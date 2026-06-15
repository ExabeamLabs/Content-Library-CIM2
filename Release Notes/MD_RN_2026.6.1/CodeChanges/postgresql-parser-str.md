# Code Changes for postgresql-parser-str (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | host |  | ['\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d+Z\s+({host}[\w\-\.]+)\spostgres', '\w+\s\d{1,2}\s+\d{2}:\d{2}:\d{2}\s+({host}[\w\-\.]+)\spostgres'] |