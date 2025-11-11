# Code Changes for microsoft-evsecurity-sk4-user-privilege-assign-success-4673 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'activity_id', 'app', 'dest_domain', 'dest_host', 'dest_login_id', 'dest_user', 'dest_user_sid', 'domain', 'event_code', 'event_id', 'event_name', 'host', 'login_id', 'login_type', 'object_server', 'os', 'privileges', 'process_dir', 'process_id', 'process_name', 'process_path', 'provider_name', 'result', 'sid_history', 'src_domain', 'src_host', 'src_user', 'task_name', 'thread_id', 'time', 'user', 'user_sid'] |
| edit_regex_field | domain |  | ['"+SubjectDomainName"+:"+({src_domain}({domain}[^"]+))'] |
| edit_regex_field | src_user |  | ['"+SubjectUserName"+:"+(SYSTEM|-|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))'] |
| edit_regex_field | user |  | ['"+SubjectUserName"+:"+(SYSTEM|-|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))', '"user"+:"+(SYSTEM|-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| added_regex_field | src_domain |  | ['"+SubjectDomainName"+:"+({src_domain}({domain}[^"]+))'] |
| removed_attribute | DupFields |  | N/A |