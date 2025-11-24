# Code Changes for tanium-ep-json-alert-trigger-success-accountenumeration (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| removed_attribute | ExtractionType |  | N/A |
| changed_parsed_fields | N/A |  | ['alert_id', 'alert_name', 'alert_type', 'domain', 'hash_md5', 'parent_process_dir', 'parent_process_name', 'parent_process_path', 'path', 'process_command_line', 'process_dir', 'process_name', 'process_path', 'src_host', 'src_ip', 'time', 'user'] |
| edit_regex_field | domain |  | ['"Match Details":\{"match":\{[^\$]+?"properties"[^\]]+?"user":"+(?:(?:NT AUTHORITY|({domain}[^\\"]+))\\+)?(?:({user}SYSTEM|LOCAL SERVICE|[\w\.\-\!\#\^\~]{1,40}\$?))"', '"user":"+(?:(?:NT AUTHORITY|({domain}[^\\"]+))\\+)?(?:SYSTEM|LOCAL SERVICE|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"\},"source'] |
| edit_regex_field | parent_process_dir |  | ['"Match Details":\{"match":\{[^\$]+?"properties"[^\]]+?"parent":\s*\{[^\]]+?file"[^\]]+?"fullpath":"(({parent_process_path}({parent_process_dir}[^"]+)\\+({parent_process_name}[^"]+)))'] |
| edit_regex_field | parent_process_name |  | ['"Match Details":\{"match":\{[^\$]+?"properties"[^\]]+?"parent":\s*\{[^\]]+?file"[^\]]+?"fullpath":"(({parent_process_path}({parent_process_dir}[^"]+)\\+({parent_process_name}[^"]+)))'] |
| edit_regex_field | parent_process_path |  | ['"Match Details":\{"match":\{[^\$]+?"properties"[^\]]+?"parent":\s*\{[^\]]+?file"[^\]]+?"fullpath":"(({parent_process_path}({parent_process_dir}[^"]+)\\+({parent_process_name}[^"]+)))'] |
| edit_regex_field | path |  | ['"Match Details":\{"match":\{[^\$]+?"properties"[^\$]+?"file"[^\]]+?"fullpath":"({path}({process_path}({process_dir}[^"]+)\\+({process_name}[^"]+)))"'] |
| edit_regex_field | process_command_line |  | ['"Match Details":\{"match":\{[^\$]+?"properties"[^\]]+?args\\?"+:"*\\*"+({process_command_line}[^,\]]+?)\\?\s*",'] |
| edit_regex_field | process_dir |  | ['"Match Details":\{"match":\{[^\$]+?"properties"[^\$]+?"file"[^\]]+?"fullpath":"({path}({process_path}({process_dir}[^"]+)\\+({process_name}[^"]+)))"'] |
| edit_regex_field | process_name |  | ['"Match Details":\{"match":\{[^\$]+?"properties"[^\$]+?"file"[^\]]+?"fullpath":"({path}({process_path}({process_dir}[^"]+)\\+({process_name}[^"]+)))"'] |
| edit_regex_field | process_path |  | ['"Match Details":\{"match":\{[^\$]+?"properties"[^\$]+?"file"[^\]]+?"fullpath":"({path}({process_path}({process_dir}[^"]+)\\+({process_name}[^"]+)))"'] |
| edit_regex_field | user |  | ['"Match Details":\{"match":\{[^\$]+?"properties"[^\]]+?"user":"+(?:(?:NT AUTHORITY|({domain}[^\\"]+))\\+)?(?:({user}SYSTEM|LOCAL SERVICE|[\w\.\-\!\#\^\~]{1,40}\$?))"', '"user":"+(?:(?:NT AUTHORITY|({domain}[^\\"]+))\\+)?(?:SYSTEM|LOCAL SERVICE|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"\},"source'] |
| added_regex_field | alert_id |  | ['"Alert Id":\s*"({alert_id}[^"]+)"'] |
| added_regex_field | alert_name |  | ['"Intel Name":\s*"({alert_name}[^"]+)"'] |
| added_regex_field | alert_type |  | ['"Intel Type":\s*"({alert_type}[^"]+)"'] |
| added_regex_field | hash_md5 |  | ['"Match Details":\{"match":\{[^\$]+?"properties"[^\]]+?md5\\?"+:"*\\*"+({hash_md5}[^,\]]+?)\\?\s*",'] |
| added_regex_field | src_host |  | ['"Computer Name":\s*"({src_host}[^"]+)"'] |
| added_regex_field | src_ip |  | ['"Computer IP":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"'] |
| added_regex_field | time |  | ['"Timestamp":\s*"({time}[^"]+)"'] |