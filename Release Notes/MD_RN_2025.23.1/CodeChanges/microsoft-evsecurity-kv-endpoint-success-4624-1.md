# Code Changes for microsoft-evsecurity-kv-endpoint-success-4624-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['auth_package', 'auth_process', 'dest_domain', 'dest_login_id', 'dest_user', 'dest_user_sid', 'domain', 'event_code', 'host', 'key_length', 'login_id', 'login_type', 'process_dir', 'process_name', 'process_path', 'src_host', 'src_host_windows', 'src_ip', 'src_port', 'src_user', 'subject_sid', 'time', 'user', 'user_sid'] |
| edit_regex_field | domain |  | ['TargetDomainName:({dest_domain}({domain}[^,]+))'] |
| edit_regex_field | login_id |  | ['TargetLogonId:({dest_login_id}({login_id}[^,]+))'] |
| edit_regex_field | src_host_windows |  | ['WorkstationName:(-|({src_host_windows}({src_host}[^,]+)))'] |
| edit_regex_field | user |  | ['TargetUserName:({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| edit_regex_field | user_sid |  | ['TargetUserSid:({dest_user_sid}({user_sid}[^,]+))'] |
| added_regex_field | dest_domain |  | ['TargetDomainName:({dest_domain}({domain}[^,]+))'] |
| added_regex_field | dest_login_id |  | ['TargetLogonId:({dest_login_id}({login_id}[^,]+))'] |
| added_regex_field | dest_user |  | ['TargetUserName:({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| added_regex_field | dest_user_sid |  | ['TargetUserSid:({dest_user_sid}({user_sid}[^,]+))'] |
| added_regex_field | src_host |  | ['WorkstationName:(-|({src_host_windows}({src_host}[^,]+)))'] |
| removed_attribute | DupFields |  | N/A |