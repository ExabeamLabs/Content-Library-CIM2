# Code Changes for microsoft-evsecurity-kv-log-clear-success-1102-3 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_id', 'account_name', 'auth_package', 'auth_process', 'client', 'dest_domain', 'dest_host', 'dest_user', 'dest_user_sid', 'domain', 'event_code', 'failure_reason', 'host', 'key_length', 'login_id', 'login_type', 'object_server', 'process_command_line', 'process_dir', 'process_guid', 'process_id', 'process_name', 'process_path', 'result_code', 'service_name', 'service_type', 'src_domain', 'src_ip', 'src_port', 'src_user', 'time', 'user', 'user_dn', 'user_sid'] |
| edit_regex_field | dest_host |  | ['Computer="+({host}({dest_host}[\w\-.]+))"'] |
| edit_regex_field | domain |  | ['SubjectDomainName="+(-|({src_domain}({domain}[^"]+)))"'] |
| edit_regex_field | user |  | ['SubjectUserName="+(-|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))"', 'SubjectUserName="+(-|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))"'] |
| added_regex_field | host |  | ['Computer="+({host}({dest_host}[\w\-.]+))"'] |
| added_regex_field | src_domain |  | ['SubjectDomainName="+(-|({src_domain}({domain}[^"]+)))"'] |
| added_regex_field | src_user |  | ['SubjectUserName="+(-|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))"', 'SubjectUserName="+(-|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))"'] |
| removed_attribute | DupFields |  | N/A |