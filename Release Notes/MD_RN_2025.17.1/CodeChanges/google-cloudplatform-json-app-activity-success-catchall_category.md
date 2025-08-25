# Code Changes for google-cloudplatform-json-app-activity-success-catchall_category (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| COULD_NOT_COMPARE | TimeFormat |  | yyyy-MM-dd'T'HH:mm:ss |
| changed_parsed_fields | N/A |  | ['email_address', 'resource_dir', 'resource_name', 'resource_path', 'src_ip', 'src_port', 'time'] |
| added_regex_field | time |  | ['exa_json_path=$..eventTime,exa_regex=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)', 'exa_json_path=$..timestamp,exa_regex=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)'] |