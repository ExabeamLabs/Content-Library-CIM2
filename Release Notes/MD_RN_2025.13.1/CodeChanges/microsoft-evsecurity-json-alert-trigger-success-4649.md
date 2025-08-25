# Code Changes for microsoft-evsecurity-json-alert-trigger-success-4649 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['auth_package', 'auth_process', 'domain', 'event_name', 'login_id', 'process_dir', 'process_name', 'process_path', 'user', 'user_sid'] |
| edit_regex_field | auth_process |  | ['exa_json_path=$..LogonProcessName,exa_regex=^(-|({auth_process}.+?))\s*$', 'exa_regex=Logon Process:\s+({auth_process}[^\s]+)'] |
| edit_regex_field | process_dir |  | ['exa_json_path=$..ProcessName,exa_regex=^({process_path}({process_dir}[^,"]*?[\\\/]+)?({process_name}[^\\\/\s"]+?))$', 'exa_regex=Process Name:\s+({process_path}(({process_dir}[^\s]+)\\+)?({process_name}[^\s]+))\s+Network Information:'] |
| edit_regex_field | process_name |  | ['exa_json_path=$..ProcessName,exa_regex=^({process_path}({process_dir}[^,"]*?[\\\/]+)?({process_name}[^\\\/\s"]+?))$', 'exa_regex=Process Name:\s+({process_path}(({process_dir}[^\s]+)\\+)?({process_name}[^\s]+))\s+Network Information:'] |
| edit_regex_field | process_path |  | ['exa_json_path=$..ProcessName,exa_regex=^({process_path}({process_dir}[^,"]*?[\\\/]+)?({process_name}[^\\\/\s"]+?))$', 'exa_regex=Process Name:\s+({process_path}(({process_dir}[^\s]+)\\+)?({process_name}[^\s]+))\s+Network Information:'] |
| edit_regex_field | user |  | ['exa_json_path=$..SubjectUserName,exa_regex=^({user}[\w\.\-\!\#\^\~]{1,40}\$?)$', 'exa_regex=Subject: Security ID:\s*({user_sid}S-[^\s]+)\s*Account Name: ({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s*Account Domain:\s*({domain}[^\s]+)\s* Logon ID:\s*({login_id}[^\s]+)'] |
| added_regex_field | auth_package |  | ['exa_regex=Authentication Package:\s+({auth_package}[^\s]+)'] |
| added_regex_field | domain |  | ['exa_regex=Subject: Security ID:\s*({user_sid}S-[^\s]+)\s*Account Name: ({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s*Account Domain:\s*({domain}[^\s]+)\s* Logon ID:\s*({login_id}[^\s]+)'] |
| added_regex_field | login_id |  | ['exa_regex=Subject: Security ID:\s*({user_sid}S-[^\s]+)\s*Account Name: ({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s*Account Domain:\s*({domain}[^\s]+)\s* Logon ID:\s*({login_id}[^\s]+)'] |
| added_regex_field | user_sid |  | ['exa_regex=Subject: Security ID:\s*({user_sid}S-[^\s]+)\s*Account Name: ({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s*Account Domain:\s*({domain}[^\s]+)\s* Logon ID:\s*({login_id}[^\s]+)'] |