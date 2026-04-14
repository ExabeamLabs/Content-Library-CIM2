# Code Changes for jamf-jamfpro-json-endpoint-notification-success-devicetelemetrystream (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['process_dir', 'process_name', 'process_path'] |
| added_regex_field | process_dir |  | ['exa_json_path=$.event.exec.dyld_exec_path,exa_regex=({process_path}({process_dir}[^"]+[\/]+)?({process_name}[^"]+))'] |
| added_regex_field | process_name |  | ['exa_json_path=$.event.exec.dyld_exec_path,exa_regex=({process_path}({process_dir}[^"]+[\/]+)?({process_name}[^"]+))'] |
| added_regex_field | process_path |  | ['exa_json_path=$.event.exec.dyld_exec_path,exa_regex=({process_path}({process_dir}[^"]+[\/]+)?({process_name}[^"]+))'] |
| edit_attribute | activity_type |  | ['endpoint-login:fail', 'endpoint-login:success', 'endpoint-notification:success'] |
| edit_attribute | legacy_activity_type |  | ['app-activity', 'computer-logon'] |