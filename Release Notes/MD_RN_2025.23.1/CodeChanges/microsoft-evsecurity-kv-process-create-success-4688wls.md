# Code Changes for microsoft-evsecurity-kv-process-create-success-4688wls (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['domain', 'event_code', 'host', 'login_id', 'parent_process_guid', 'path', 'process_command_line', 'process_dir', 'process_guid', 'process_id', 'process_name', 'process_path', 'service_name', 'src_domain', 'src_user', 'user', 'user_sid'] |
| edit_regex_field | domain |  | ['SubjectDomainName="+(?=\w)({src_domain}({domain}[^"]+))"'] |
| edit_regex_field | user |  | ['SubjectUserName="+(?=\w)({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))"'] |
| added_regex_field | src_domain |  | ['SubjectDomainName="+(?=\w)({src_domain}({domain}[^"]+))"'] |
| added_regex_field | src_user |  | ['SubjectUserName="+(?=\w)({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))"'] |
| removed_attribute | DupFields |  | N/A |