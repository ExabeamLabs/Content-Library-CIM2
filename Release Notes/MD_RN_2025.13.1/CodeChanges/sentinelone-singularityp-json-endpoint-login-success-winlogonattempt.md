# Code Changes for sentinelone-singularityp-json-endpoint-login-success-winlogonattempt (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_ip', 'dest_port', 'domain', 'file_dir', 'file_name', 'file_path', 'src_ip', 'src_port', 'user'] |
| added_regex_field | file_dir |  | ['exa_json_path=$.sourceProcessInfo.filePath,exa_regex=^(({file_path}({file_dir}[^"]+?[\\\/]+)({file_name}[^"\\\/]+(\.([a-zA-Z]+))))|({=file_dir}[^"]+))'] |
| added_regex_field | file_name |  | ['exa_json_path=$.sourceProcessInfo.filePath,exa_regex=^(({file_path}({file_dir}[^"]+?[\\\/]+)({file_name}[^"\\\/]+(\.([a-zA-Z]+))))|({=file_dir}[^"]+))'] |
| added_regex_field | file_path |  | ['exa_json_path=$.sourceProcessInfo.filePath,exa_regex=^(({file_path}({file_dir}[^"]+?[\\\/]+)({file_name}[^"\\\/]+(\.([a-zA-Z]+))))|({=file_dir}[^"]+))'] |