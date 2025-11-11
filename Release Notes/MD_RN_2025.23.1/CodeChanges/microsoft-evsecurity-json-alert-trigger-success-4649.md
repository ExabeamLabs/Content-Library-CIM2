# Code Changes for microsoft-evsecurity-json-alert-trigger-success-4649 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['alert_name', 'alert_type', 'auth_package', 'auth_process', 'domain', 'event_name', 'login_id', 'process_dir', 'process_name', 'process_path', 'src_domain', 'src_user', 'user', 'user_sid'] |
| edit_regex_field | auth_process |  | ['exa_json_path=$..LogonProcessName,exa_regex=^(-|({alert_type}({auth_process}.+?)))\s*$', 'exa_regex=Logon Process:\s+({alert_type}({auth_process}[^\s]+))'] |
| edit_regex_field | domain |  | ['exa_regex=Subject: Security ID:\s*({user_sid}S-[^\s]+)\s*Account Name: ({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*Account Domain:\s*({src_domain}({domain}[^\s]+))\s* Logon ID:\s*({login_id}[^\s]+)'] |
| edit_regex_field | event_name |  | ['exa_json_path=$.Message,exa_regex=({alert_name}({event_name}[^\.]+)).\s*Subject'] |
| edit_regex_field | login_id |  | ['exa_regex=Subject: Security ID:\s*({user_sid}S-[^\s]+)\s*Account Name: ({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*Account Domain:\s*({src_domain}({domain}[^\s]+))\s* Logon ID:\s*({login_id}[^\s]+)'] |
| edit_regex_field | user |  | ['exa_json_path=$..SubjectUserName,exa_regex=^({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))$', 'exa_regex=Subject: Security ID:\s*({user_sid}S-[^\s]+)\s*Account Name: ({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*Account Domain:\s*({src_domain}({domain}[^\s]+))\s* Logon ID:\s*({login_id}[^\s]+)'] |
| edit_regex_field | user_sid |  | ['exa_regex=Subject: Security ID:\s*({user_sid}S-[^\s]+)\s*Account Name: ({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*Account Domain:\s*({src_domain}({domain}[^\s]+))\s* Logon ID:\s*({login_id}[^\s]+)'] |
| added_regex_field | alert_name |  | ['exa_json_path=$.Message,exa_regex=({alert_name}({event_name}[^\.]+)).\s*Subject'] |
| added_regex_field | alert_type |  | ['exa_json_path=$..LogonProcessName,exa_regex=^(-|({alert_type}({auth_process}.+?)))\s*$', 'exa_regex=Logon Process:\s+({alert_type}({auth_process}[^\s]+))'] |
| added_regex_field | src_domain |  | ['exa_regex=Subject: Security ID:\s*({user_sid}S-[^\s]+)\s*Account Name: ({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*Account Domain:\s*({src_domain}({domain}[^\s]+))\s* Logon ID:\s*({login_id}[^\s]+)'] |
| added_regex_field | src_user |  | ['exa_json_path=$..SubjectUserName,exa_regex=^({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))$', 'exa_regex=Subject: Security ID:\s*({user_sid}S-[^\s]+)\s*Account Name: ({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*Account Domain:\s*({src_domain}({domain}[^\s]+))\s* Logon ID:\s*({login_id}[^\s]+)'] |
| removed_attribute | DupFields |  | N/A |