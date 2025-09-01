# Code Changes for windows-events-1 (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | time |  | ['({time}\d+-\d+-\d+T\d+:\d+:\d+)', 'SystemTime=(\'|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)', 'SystemTime=(\'|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d{1,9}Z)', '\srt=({time}\d{13})'] |