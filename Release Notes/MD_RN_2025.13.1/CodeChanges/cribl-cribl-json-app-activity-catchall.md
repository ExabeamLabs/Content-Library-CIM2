# Code Changes for cribl-cribl-json-app-activity-catchall (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['file_dir', 'file_name', 'file_path', 'src_ip', 'src_port'] |
| edit_regex_field | file_name |  | ['exa_regex="file":"({file_path}({file_dir}[^"]*\/)?({file_name}[^"]+))'] |
| edit_regex_field | file_path |  | ['exa_regex="file":"({file_path}({file_dir}[^"]*\/)?({file_name}[^"]+))'] |
| added_regex_field | file_dir |  | ['exa_regex="file":"({file_path}({file_dir}[^"]*\/)?({file_name}[^"]+))'] |