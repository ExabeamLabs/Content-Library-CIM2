# Code Changes for citrix-sharefile-cef-file-download-success-download (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'additional_info', 'app', 'company', 'country_code', 'email_address', 'email_domain', 'event_code', 'file_dir', 'file_ext', 'file_name', 'file_path', 'full_name', 'operation', 'src_file_ext', 'src_file_name', 'src_file_path', 'src_ip', 'src_port', 'time', 'uri_path'] |
| edit_regex_field | file_dir |  | ['"ItemName"+:"+({src_file_path}({file_path}({file_dir}[^"]*[\/]+)\s*({src_file_name}({file_name}[^\/"]+(\.({src_file_ext}({file_ext}[^\/"]+)))))))"'] |
| edit_regex_field | file_ext |  | ['"ItemName"+:"+({src_file_path}({file_path}({file_dir}[^"]*[\/]+)\s*({src_file_name}({file_name}[^\/"]+(\.({src_file_ext}({file_ext}[^\/"]+)))))))"'] |
| edit_regex_field | file_name |  | ['"ItemName"+:"+({src_file_path}({file_path}({file_dir}[^"]*[\/]+)\s*({src_file_name}({file_name}[^\/"]+(\.({src_file_ext}({file_ext}[^\/"]+)))))))"'] |
| edit_regex_field | file_path |  | ['"ItemName"+:"+({src_file_path}({file_path}({file_dir}[^"]*[\/]+)\s*({src_file_name}({file_name}[^\/"]+(\.({src_file_ext}({file_ext}[^\/"]+)))))))"'] |
| added_regex_field | src_file_ext |  | ['"ItemName"+:"+({src_file_path}({file_path}({file_dir}[^"]*[\/]+)\s*({src_file_name}({file_name}[^\/"]+(\.({src_file_ext}({file_ext}[^\/"]+)))))))"'] |
| added_regex_field | src_file_name |  | ['"ItemName"+:"+({src_file_path}({file_path}({file_dir}[^"]*[\/]+)\s*({src_file_name}({file_name}[^\/"]+(\.({src_file_ext}({file_ext}[^\/"]+)))))))"'] |
| added_regex_field | src_file_path |  | ['"ItemName"+:"+({src_file_path}({file_path}({file_dir}[^"]*[\/]+)\s*({src_file_name}({file_name}[^\/"]+(\.({src_file_ext}({file_ext}[^\/"]+)))))))"'] |
| removed_attribute | DupFields |  | N/A |