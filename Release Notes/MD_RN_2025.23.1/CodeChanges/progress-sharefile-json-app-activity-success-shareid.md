# Code Changes for progress-sharefile-json-app-activity-success-shareid (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['app', 'email_address', 'email_domain', 'file_dir', 'file_ext', 'file_name', 'file_path', 'src_file_ext', 'src_file_name', 'src_file_path', 'time'] |
| edit_regex_field | file_dir |  | ['exa_regex="Name":\s*"({src_file_path}({file_path}({file_dir}[^"]*?[\/]+)?({src_file_name}({file_name}[^\/"]+?(\.({src_file_ext}({file_ext}[^.\/"]+)))?))))"'] |
| edit_regex_field | file_ext |  | ['exa_regex="Name":\s*"({src_file_path}({file_path}({file_dir}[^"]*?[\/]+)?({src_file_name}({file_name}[^\/"]+?(\.({src_file_ext}({file_ext}[^.\/"]+)))?))))"'] |
| edit_regex_field | file_name |  | ['exa_regex="Name":\s*"({src_file_path}({file_path}({file_dir}[^"]*?[\/]+)?({src_file_name}({file_name}[^\/"]+?(\.({src_file_ext}({file_ext}[^.\/"]+)))?))))"'] |
| edit_regex_field | file_path |  | ['exa_regex="Name":\s*"({src_file_path}({file_path}({file_dir}[^"]*?[\/]+)?({src_file_name}({file_name}[^\/"]+?(\.({src_file_ext}({file_ext}[^.\/"]+)))?))))"'] |
| added_regex_field | src_file_ext |  | ['exa_regex="Name":\s*"({src_file_path}({file_path}({file_dir}[^"]*?[\/]+)?({src_file_name}({file_name}[^\/"]+?(\.({src_file_ext}({file_ext}[^.\/"]+)))?))))"'] |
| added_regex_field | src_file_name |  | ['exa_regex="Name":\s*"({src_file_path}({file_path}({file_dir}[^"]*?[\/]+)?({src_file_name}({file_name}[^\/"]+?(\.({src_file_ext}({file_ext}[^.\/"]+)))?))))"'] |
| added_regex_field | src_file_path |  | ['exa_regex="Name":\s*"({src_file_path}({file_path}({file_dir}[^"]*?[\/]+)?({src_file_name}({file_name}[^\/"]+?(\.({src_file_ext}({file_ext}[^.\/"]+)))?))))"'] |
| removed_attribute | DupFields |  | N/A |