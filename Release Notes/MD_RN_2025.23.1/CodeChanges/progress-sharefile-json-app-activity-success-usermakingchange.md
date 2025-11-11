# Code Changes for progress-sharefile-json-app-activity-success-usermakingchange (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['app', 'email_address', 'email_domain', 'file_dir', 'file_ext', 'file_name', 'file_path', 'src_file_dir', 'src_file_ext', 'src_file_name', 'src_file_path', 'src_ip', 'src_port'] |
| added_regex_field | src_file_dir |  | ['exa_regex="Path":\s*"({src_file_path}\/*({src_file_dir}[^"]*?[\/]+)?({src_file_name}[^\/",]+?(\.({src_file_ext}[^\/"\.\s,]+))?))"'] |
| added_regex_field | src_file_ext |  | ['exa_regex="Path":\s*"({src_file_path}\/*({src_file_dir}[^"]*?[\/]+)?({src_file_name}[^\/",]+?(\.({src_file_ext}[^\/"\.\s,]+))?))"'] |
| added_regex_field | src_file_name |  | ['exa_regex="Path":\s*"({src_file_path}\/*({src_file_dir}[^"]*?[\/]+)?({src_file_name}[^\/",]+?(\.({src_file_ext}[^\/"\.\s,]+))?))"'] |
| added_regex_field | src_file_path |  | ['exa_regex="Path":\s*"({src_file_path}\/*({src_file_dir}[^"]*?[\/]+)?({src_file_name}[^\/",]+?(\.({src_file_ext}[^\/"\.\s,]+))?))"'] |
| removed_attribute | DupFields |  | N/A |