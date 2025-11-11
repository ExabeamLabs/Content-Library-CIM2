# Code Changes for microsoft-sysmon-json-process-create-success-createremotethread (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_process', 'dest_process_dir', 'dest_process_name', 'dest_process_path', 'process_dir', 'process_name', 'process_path', 'user'] |
| edit_regex_field | dest_process_dir |  | ['exa_json_path=$.TargetImage,exa_regex=({dest_process}({dest_process_path}(({dest_process_dir}[^"]*?)[\\\/]+)?({dest_process_name}[^"\\\/]+)))"'] |
| edit_regex_field | dest_process_name |  | ['exa_json_path=$.TargetImage,exa_regex=({dest_process}({dest_process_path}(({dest_process_dir}[^"]*?)[\\\/]+)?({dest_process_name}[^"\\\/]+)))"'] |
| edit_regex_field | dest_process_path |  | ['exa_json_path=$.TargetImage,exa_regex=({dest_process}({dest_process_path}(({dest_process_dir}[^"]*?)[\\\/]+)?({dest_process_name}[^"\\\/]+)))"'] |
| added_regex_field | dest_process |  | ['exa_json_path=$.TargetImage,exa_regex=({dest_process}({dest_process_path}(({dest_process_dir}[^"]*?)[\\\/]+)?({dest_process_name}[^"\\\/]+)))"'] |
| removed_attribute | DupFields |  | N/A |