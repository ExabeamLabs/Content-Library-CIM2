# Code Changes for fireeye-helix-json-alert-trigger-success-alerts (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['domain', 'file_name', 'file_path', 'operation', 'process_command_line', 'process_dir', 'process_id', 'process_name', 'process_path', 'user'] |
| edit_regex_field | process_name |  | ['exa_regex=\Wprocess":\s*"({process_name}[^"]+)"', 'exa_regex=\WprocessPath":\s*"(({process_path}({process_dir}[^"]+?[\\\/]+)({process_name}[^"\\\/]+(\.[a-zA-Z]+)))|({=process_dir}[^"]+))"'] |
| edit_regex_field | process_path |  | ['exa_regex=\WprocessPath":\s*"(({process_path}({process_dir}[^"]+?[\\\/]+)({process_name}[^"\\\/]+(\.[a-zA-Z]+)))|({=process_dir}[^"]+))"'] |
| added_regex_field | process_dir |  | ['exa_regex=\WprocessPath":\s*"(({process_path}({process_dir}[^"]+?[\\\/]+)({process_name}[^"\\\/]+(\.[a-zA-Z]+)))|({=process_dir}[^"]+))"'] |