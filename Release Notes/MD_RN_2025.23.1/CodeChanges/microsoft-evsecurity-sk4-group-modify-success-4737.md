# Code Changes for microsoft-evsecurity-sk4-group-modify-success-4737 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_domain', 'action', 'activity_id', 'app', 'dest_user', 'domain', 'event_code', 'event_id', 'event_name', 'group_domain', 'group_name', 'host', 'key_name', 'key_type', 'login_id', 'login_type', 'operation', 'os', 'privileges', 'process_id', 'provider_name', 'result', 'sid_history', 'src_domain', 'src_host', 'src_user', 'task_name', 'thread_id', 'time', 'user', 'user_sid'] |
| edit_regex_field | user |  | ['"+SubjectUserName"+:"+(SYSTEM|({user}[\w\.\-\!\#\^\~]{1,40}\$?))', '"user"+:"+(SYSTEM|({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| added_regex_field | domain |  | ['"+SubjectDomainName"+:"+({domain}[^"]+)'] |
| removed_attribute | DupFields |  | N/A |