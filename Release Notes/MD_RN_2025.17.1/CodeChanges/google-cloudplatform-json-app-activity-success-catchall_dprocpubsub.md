# Code Changes for google-cloudplatform-json-app-activity-success-catchall_dprocpubsub (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | time |  | ['exa_json_path=$.time,exa_regex=({time}\d{10})', 'exa_regex="timestamp":"({time}\d\d.\d\d.\d\d\d\d\s\d\d:\d\d:\d\d)"', 'exa_regex="timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)'] |