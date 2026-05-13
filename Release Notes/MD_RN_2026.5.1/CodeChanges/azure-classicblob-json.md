# Code Changes for azure-classicblob-json (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | bytes_in |  | ['"+properties"+:[^\}]+"+requestBodySize"+:\s*({bytes_in}\d+)', 'exa_json_path=$..requestBodySize,exa_regex=({bytes_in}\d+)'] |
| edit_regex_field | bytes_out |  | ['"+properties"+:[^\}]+"+responseBodySize"+:\s*({bytes_out}\d+)', 'exa_json_path=$..responseBodySize,exa_regex=({bytes_out}\d+)'] |
| edit_regex_field | time |  | ['"+time"+:\s*"+({time}\d+-\d+-\d+T\d+:\d+:\d+.\d+Z?)"+', 'exa_regex="time":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\d\d\d\d\dZ)'] |