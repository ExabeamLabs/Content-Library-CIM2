# Code Changes for progress-sharefile-json-app-activity-eventid (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['app', 'country_code', 'email_address', 'email_domain', 'failure_reason', 'file_dir', 'file_ext', 'file_name', 'file_path', 'src_file_dir', 'src_file_ext', 'src_file_name', 'src_file_path', 'src_ip', 'src_port', 'time'] |
| added_regex_field | src_file_dir |  | ['exa_regex="ItemName":\s*"({src_file_path}({src_file_dir}[^"]*[\/]+)\s*({src_file_name}[^\/"]+(\.({src_file_ext}[^\/"]+))))"'] |
| added_regex_field | src_file_ext |  | ['exa_regex="ItemName":\s*"({src_file_path}({src_file_dir}[^"]*[\/]+)\s*({src_file_name}[^\/"]+(\.({src_file_ext}[^\/"]+))))"'] |
| added_regex_field | src_file_name |  | ['exa_regex="ItemName":\s*"({src_file_path}({src_file_dir}[^"]*[\/]+)\s*({src_file_name}[^\/"]+(\.({src_file_ext}[^\/"]+))))"'] |
| added_regex_field | src_file_path |  | ['exa_regex="ItemName":\s*"({src_file_path}({src_file_dir}[^"]*[\/]+)\s*({src_file_name}[^\/"]+(\.({src_file_ext}[^\/"]+))))"'] |
| removed_attribute | DupFields |  | N/A |