# Code Changes for airlock-allowlisting-json-app-activity-success-fileactivity (Parser)

| Code Change | Field Name | 2025.11.1 | 2025.12.1 |
|-------------|------------|-----------|------------|
| changed_parsed_fields | N/A | ['email_address', 'event_name', 'file_ext', 'file_name', 'host', 'user'] | ['email_address', 'event_name', 'file_ext', 'file_name', 'host', 'process_dir', 'process_name', 'process_path', 'user'] |
| added_regex_field | process_dir | [] | ['exa_json_path=$.parentprocess,exa_regex=^({process_path}({process_dir}[^=]*[\\\/]+)?({process_name}[^=]+?))$'] |
| added_regex_field | process_name | [] | ['exa_json_path=$.parentprocess,exa_regex=^({process_path}({process_dir}[^=]*[\\\/]+)?({process_name}[^=]+?))$'] |
| added_regex_field | process_path | [] | ['exa_json_path=$.parentprocess,exa_regex=^({process_path}({process_dir}[^=]*[\\\/]+)?({process_name}[^=]+?))$'] |