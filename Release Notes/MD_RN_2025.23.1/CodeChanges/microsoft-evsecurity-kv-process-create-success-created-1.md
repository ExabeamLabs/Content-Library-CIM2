# Code Changes for microsoft-evsecurity-kv-process-create-success-created-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_process_dir', 'dest_process_name', 'dest_process_path', 'dest_user', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'parameter_csproj', 'parameter_dll', 'parameter_exe', 'parameter_hta', 'parameter_sct', 'parameter_xml', 'parent_process_dir', 'parent_process_guid', 'parent_process_id', 'parent_process_name', 'parent_process_path', 'process_command_line', 'process_dir', 'process_guid', 'process_id', 'process_name', 'process_path', 'service_command_line', 'service_name', 'src_domain', 'src_host', 'src_ip', 'src_user', 'time', 'user'] |
| edit_regex_field | domain |  | ['Account Domain:(\\+[rnt]|\s)*(-|({domain}[^\s]+?))(\\+[rnt]|\s|;)*Logon ID:', 'Creator Subject:.+?Account Domain:(\\+[rnt]|\s)*(-|({domain}[^\s]+?))(\\+[rnt]|\s|;)*Logon ID:', '\"SubjectDomainName\\?":\\?"({src_domain}({domain}[^\\"]+))'] |
| edit_regex_field | parent_process_guid |  | ['Creator Process ID:(\\+[rnt]|\s)*({parent_process_id}({parent_process_guid}[^\\\s;]+))(\s|\\+[rnt]|;|\\)'] |
| edit_regex_field | process_guid |  | ['New Process ID:((\\)*(\\t|\\r|\\n))*\s*({process_id}({process_guid}[^\\\s;]+))(\s|;|\\)'] |
| edit_regex_field | src_domain |  | ['\"SubjectDomainName\\?":\\?"({src_domain}({domain}[^\\"]+))'] |
| edit_regex_field | src_user |  | ['SubjectUserName\\?"+:\\?"+(?:-|(?i)(LOCAL SYSTEM|anonymous logon|LOCAL SERVICE|SYSTEM)|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\\?"'] |
| edit_regex_field | user |  | ["Creator Subject:.+?Account Name:(\\+[rnt]|\s)*'?(-|({user}LOCAL SERVICE|SYSTEM|Administrator|NETWORK SERVICE|[\w\.\-\!\#\^\~]{1,40}\$?))", 'Subject:.+?Account Name:\s*(-|SYSTEM|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*\w+\s\w+:', 'SubjectUserName\\?"+:\\?"+(?:-|(?i)(LOCAL SYSTEM|anonymous logon|LOCAL SERVICE|SYSTEM)|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\\?"'] |
| added_regex_field | parent_process_id |  | ['Creator Process ID:(\\+[rnt]|\s)*({parent_process_id}({parent_process_guid}[^\\\s;]+))(\s|\\+[rnt]|;|\\)'] |
| added_regex_field | process_id |  | ['New Process ID:((\\)*(\\t|\\r|\\n))*\s*({process_id}({process_guid}[^\\\s;]+))(\s|;|\\)'] |
| removed_attribute | DupFields |  | N/A |