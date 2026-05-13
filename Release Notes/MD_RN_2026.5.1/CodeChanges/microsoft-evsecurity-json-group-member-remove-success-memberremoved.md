# Code Changes for microsoft-evsecurity-json-group-member-remove-success-memberremoved (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_id', 'action', 'activity_id', 'app', 'dest_domain', 'dest_login_id', 'dest_user', 'dest_user_sid', 'domain', 'event_code', 'event_id', 'event_name', 'group_domain', 'group_id', 'group_name', 'host', 'login_id', 'login_type', 'os', 'privileges', 'process_id', 'provider_name', 'result', 'sid_history', 'src_domain', 'src_host', 'src_user', 'task_name', 'thread_id', 'time', 'user', 'user_sid'] |
| edit_regex_field | group_id |  | ['"Group":[^}]+?"Security ID"\s*:"({group_id}[^"]+)', '"TargetSid":"({group_id}[^\s"]+)'] |
| added_regex_field | group_domain |  | ['"Group":[^}]+?"(Group|Account) Domain"\s*:"({group_domain}[^"]+)'] |
| added_regex_field | group_name |  | ['"Group":[^}]+?"(Group|Account) Name"\s*:"({group_name}[^"]+)'] |