# Code Changes for microsoft-evsecurity-kv-user-delete-fail-logtype (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_id', 'account_name', 'auth_process', 'client', 'dest_domain', 'dest_host', 'dest_user', 'dest_user_sid', 'domain', 'event_code', 'failure_reason', 'http_response_code', 'key_length', 'login_id', 'login_type', 'object_server', 'process_command_line', 'process_dir', 'process_guid', 'process_id', 'process_name', 'process_path', 'service_name', 'service_type', 'src_domain', 'src_user', 'time', 'user', 'user_dn', 'user_sid'] |
| edit_regex_field | domain |  | ['SubjectDomainName=\"+(-|({src_domain}({domain}[^\"]+)))\"'] |
| edit_regex_field | user |  | ['SubjectUserName=\"+(-|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\"', 'SubjectUserName=\"+(-|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\"'] |
| added_regex_field | src_domain |  | ['SubjectDomainName=\"+(-|({src_domain}({domain}[^\"]+)))\"'] |
| added_regex_field | src_user |  | ['SubjectUserName=\"+(-|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\"', 'SubjectUserName=\"+(-|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\"'] |
| removed_attribute | DupFields |  | N/A |