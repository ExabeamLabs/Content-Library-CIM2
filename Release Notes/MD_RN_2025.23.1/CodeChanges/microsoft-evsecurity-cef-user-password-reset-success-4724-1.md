# Code Changes for microsoft-evsecurity-cef-user-password-reset-success-4724-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'activity_id', 'app', 'dest_domain', 'dest_host', 'dest_login_id', 'dest_user', 'dest_user_sid', 'domain', 'event_code', 'event_id', 'event_name', 'host', 'login_id', 'login_type', 'os', 'privileges', 'process_id', 'provider_name', 'result', 'sid_history', 'src_domain', 'src_host', 'src_user', 'task_name', 'thread_id', 'time', 'user', 'user_sid'] |
| edit_regex_field | domain |  | ['"+SubjectDomainName"+:"+({src_domain}({domain}[^"]+))'] |
| edit_regex_field | host |  | ['"hostname"+:"+({dest_host}({host}[\w\-.]+))'] |
| edit_regex_field | src_user |  | ['"+SubjectUserName"+:"+(SYSTEM|-|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))'] |
| edit_regex_field | user |  | ['"+SubjectUserName"+:"+(SYSTEM|-|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))', '"user"+:"+(SYSTEM|-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| added_regex_field | dest_host |  | ['"hostname"+:"+({dest_host}({host}[\w\-.]+))'] |
| added_regex_field | src_domain |  | ['"+SubjectDomainName"+:"+({src_domain}({domain}[^"]+))'] |
| removed_attribute | DupFields |  | N/A |