# Code Changes for vmware-carbonblackedr-json-alert-trigger-success-feed (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_ip', 'dest_port', 'domain', 'path', 'process_dir', 'process_name', 'process_path', 'time', 'user'] |
| edit_regex_field | process_dir |  | ['exa_json_path=$.docs[*].path,exa_regex=({path}({process_path}({process_dir}([^\"]+)?[\\\/])?({process_name}[^\\\/\"]+)))'] |
| edit_regex_field | process_name |  | ['exa_json_path=$.docs[*].path,exa_regex=({path}({process_path}({process_dir}([^\"]+)?[\\\/])?({process_name}[^\\\/\"]+)))'] |
| edit_regex_field | process_path |  | ['exa_json_path=$.docs[*].path,exa_regex=({path}({process_path}({process_dir}([^\"]+)?[\\\/])?({process_name}[^\\\/\"]+)))'] |
| added_regex_field | path |  | ['exa_json_path=$.docs[*].path,exa_regex=({path}({process_path}({process_dir}([^\"]+)?[\\\/])?({process_name}[^\\\/\"]+)))'] |
| removed_attribute | DupFields |  | N/A |