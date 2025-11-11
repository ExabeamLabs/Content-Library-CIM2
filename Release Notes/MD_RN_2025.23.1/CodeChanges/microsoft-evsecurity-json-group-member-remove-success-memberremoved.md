# Code Changes for microsoft-evsecurity-json-group-member-remove-success-memberremoved (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_id', 'action', 'activity_id', 'app', 'dest_domain', 'dest_login_id', 'dest_user', 'dest_user_sid', 'domain', 'event_code', 'event_id', 'event_name', 'group_id', 'host', 'login_id', 'login_type', 'os', 'privileges', 'process_id', 'provider_name', 'result', 'sid_history', 'src_domain', 'src_host', 'src_user', 'task_name', 'thread_id', 'time', 'user', 'user_sid'] |
| edit_regex_field | domain |  | ['"+SubjectDomainName"+:"+({src_domain}({domain}[^"]+))'] |
| edit_regex_field | user |  | ['"+SubjectUserName"+:"+(SYSTEM|-|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))', '"user"+:"+(SYSTEM|-|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))'] |
| added_regex_field | src_domain |  | ['"+SubjectDomainName"+:"+({src_domain}({domain}[^"]+))'] |
| added_regex_field | src_user |  | ['"+SubjectUserName"+:"+(SYSTEM|-|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))', '"user"+:"+(SYSTEM|-|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))'] |
| removed_attribute | DupFields |  | N/A |