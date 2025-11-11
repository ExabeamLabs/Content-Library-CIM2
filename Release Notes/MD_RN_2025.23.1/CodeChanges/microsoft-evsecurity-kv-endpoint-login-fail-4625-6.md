# Code Changes for microsoft-evsecurity-kv-endpoint-login-fail-4625-6 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['auth_package', 'auth_process', 'dest_domain', 'dest_host', 'dest_user', 'dest_user_sid', 'domain', 'event_code', 'event_id', 'failure_reason', 'host', 'login_type', 'result_code', 'src_domain', 'src_host', 'src_host_windows', 'src_ip', 'src_port', 'src_user', 'time', 'user', 'user_sid'] |
| edit_regex_field | domain |  | ['TargetDomainName="(?:-|({dest_domain}({domain}[^"]+)))', 'TargetUserName="+(?=\w)({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))(?:@({dest_domain}({domain}[^\s]+)))?"'] |
| edit_regex_field | host |  | ['Computer="+({dest_host}({host}[^"]+))"'] |
| edit_regex_field | src_host_windows |  | ['WorkstationName="+(-|({src_host_windows}({src_host}[\w\-\.]+)))"'] |
| edit_regex_field | user |  | ['TargetUserName="+(?=\w)({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))(?:@({dest_domain}({domain}[^\s]+)))?"'] |
| edit_regex_field | user_sid |  | ['TargetUserSid="+({dest_user_sid}({user_sid}[^"]+))"'] |
| added_regex_field | dest_domain |  | ['TargetDomainName="(?:-|({dest_domain}({domain}[^"]+)))', 'TargetUserName="+(?=\w)({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))(?:@({dest_domain}({domain}[^\s]+)))?"'] |
| added_regex_field | dest_host |  | ['Computer="+({dest_host}({host}[^"]+))"'] |
| added_regex_field | dest_user |  | ['TargetUserName="+(?=\w)({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))(?:@({dest_domain}({domain}[^\s]+)))?"'] |
| added_regex_field | dest_user_sid |  | ['TargetUserSid="+({dest_user_sid}({user_sid}[^"]+))"'] |
| added_regex_field | src_host |  | ['WorkstationName="+(-|({src_host_windows}({src_host}[\w\-\.]+)))"'] |
| removed_attribute | DupFields |  | N/A |