# Code Changes for microsoft-windows-sk4-dll-load-success-4610 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A | ['auth_package', 'domain', 'event_code', 'event_name', 'host', 'log_source', 'login_id', 'src_ip', 'src_port', 'time', 'user', 'user_sid'] | ['auth_package', 'domain', 'event_code', 'event_name', 'file_dir', 'file_name', 'file_path', 'host', 'log_source', 'login_id', 'src_ip', 'src_port', 'time', 'user', 'user_sid'] |
| edit_regex_field | auth_package | ['"AuthenticationPackageName":"({auth_package}[^"]+)"'] | ['"AuthenticationPackageName":"({file_path}({file_dir}[^<]+)\\({file_name}[^:]+?))\s*:\s*({auth_package}[^<]+)"'] |
| added_regex_field | file_dir | [] | ['"AuthenticationPackageName":"({file_path}({file_dir}[^<]+)\\({file_name}[^:]+?))\s*:\s*({auth_package}[^<]+)"'] |
| added_regex_field | file_name | [] | ['"AuthenticationPackageName":"({file_path}({file_dir}[^<]+)\\({file_name}[^:]+?))\s*:\s*({auth_package}[^<]+)"'] |
| added_regex_field | file_path | [] | ['"AuthenticationPackageName":"({file_path}({file_dir}[^<]+)\\({file_name}[^:]+?))\s*:\s*({auth_package}[^<]+)"'] |