# Code Changes for google-cloudplatform-json-network-traffic-success-payload (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_attribute | TimeFormat |  | yyyy-MM-dd'T'HH:mm:ss |
| edit_regex_field | time |  | ['"start_time":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)', '"timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)', 'exa_json_path=$.jsonPayload.start_time,exa_regex=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)', 'exa_json_path=$.timestamp,exa_regex=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)', 'exa_regex="start_time":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)'] |