# Code Changes for google-cloudplatform-mix-app-activity-success-prototpayload (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| COULD_NOT_COMPARE | TimeFormat |  | yyyy-MM-dd'T'HH:mm:ss |
| changed_parsed_fields | N/A |  | ['app', 'bucket_name', 'email_address', 'email_domain', 'event_category', 'failure_reason', 'host', 'operation', 'operation_first', 'operation_last', 'principal_name', 'project_id', 'region', 'resource_dir', 'resource_name', 'resource_path', 'resource_type', 'result_code', 'service_name', 'src_ip', 'src_port', 'time', 'user', 'user_agent'] |
| edit_regex_field | time |  | ['"timestamp":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)', 'exa_json_path=$.timestamp,exa_regex=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)'] |
| added_regex_field | principal_name |  | ['exa_regex=principalEmail":"({principal_name}[^"\@}]+)"', 'principalEmail":"({principal_name}[^"\@}]+)"'] |