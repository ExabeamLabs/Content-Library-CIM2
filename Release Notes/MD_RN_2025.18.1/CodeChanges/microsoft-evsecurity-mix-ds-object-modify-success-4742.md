# Code Changes for microsoft-evsecurity-mix-ds-object-modify-success-4742 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | time |  | ['"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)', '({time}\d+-\d+-\d+T\d+:\d+:\d+\.\d+)', 'EventTime":"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"', 'SystemTime=(\'|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)', '\srt=({time}\d{13})'] |