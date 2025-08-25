# Code Changes for google-cloudplatform-json-scheduled-success-scheduler (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| COULD_NOT_COMPARE | TimeFormat |  | yyyy-MM-dd'T'HH:mm:ss |
| edit_regex_field | time |  | ['"timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)', 'exa_json_path=$..timestamp,exa_regex=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)'] |