# Code Changes for microsoft-evsecurity-kv-group-member-remove-success-computer (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_domain', 'account_id', 'account_name', 'action', 'activity_id', 'channel', 'dest_user_sid', 'domain', 'event_code', 'event_id', 'event_name', 'group_domain', 'group_id', 'group_name', 'group_type', 'host', 'login_id', 'member', 'os', 'process_id', 'result', 'src_host', 'task_name', 'thread_id', 'time', 'user', 'user_dn', 'user_ou', 'user_sid'] |
| added_regex_field | channel |  | ['"channel\\*?":\\*?"({channel}[^"\\]+)'] |