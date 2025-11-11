# Code Changes for microsoft-evsecurity-json-endpoint-login-success-4624 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['auth_package', 'auth_process', 'dest_domain', 'dest_host', 'dest_ip', 'dest_login_id', 'dest_port', 'dest_user', 'dest_user_sid', 'domain', 'event_code', 'event_name', 'host', 'key_length', 'login_id', 'login_type', 'process_name', 'process_path', 'src_host_windows', 'src_ip', 'src_port', 'subject_sid', 'time', 'user', 'user_sid'] |
| edit_regex_field | domain |  | ['"TargetDomainName":"({dest_domain}({domain}[^"]*))'] |
| edit_regex_field | host |  | ['"(Hostname|MachineName|hostname)":"({dest_host}({host}[\w\-.]*))', '"Computer":"({dest_host}({host}[\w\-.]+))'] |
| edit_regex_field | login_id |  | ['"TargetLogonId":"({dest_login_id}({login_id}[^"]*))'] |
| edit_regex_field | user |  | ['"TargetUserName":"({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| edit_regex_field | user_sid |  | ['"TargetUserSid":"({dest_user_sid}({user_sid}[^"]*))'] |
| added_regex_field | dest_domain |  | ['"TargetDomainName":"({dest_domain}({domain}[^"]*))'] |
| added_regex_field | dest_host |  | ['"(Hostname|MachineName|hostname)":"({dest_host}({host}[\w\-.]*))', '"Computer":"({dest_host}({host}[\w\-.]+))'] |
| added_regex_field | dest_login_id |  | ['"TargetLogonId":"({dest_login_id}({login_id}[^"]*))'] |
| added_regex_field | dest_user |  | ['"TargetUserName":"({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| added_regex_field | dest_user_sid |  | ['"TargetUserSid":"({dest_user_sid}({user_sid}[^"]*))'] |
| removed_attribute | DupFields |  | N/A |