# Code Changes for microsoft-evsecurity-sk4-user-name-modify-4781 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_domain', 'action', 'activity_id', 'app', 'channel', 'dest_host', 'dest_user', 'domain', 'event_code', 'event_id', 'event_name', 'host', 'key_name', 'key_type', 'login_id', 'login_type', 'new_user_name', 'old_user_name', 'operation', 'os', 'privileges', 'process_id', 'provider_name', 'result', 'sid_history', 'src_domain', 'src_host', 'src_user', 'task_name', 'thread_id', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['"channel\\?"+:\\?"+({channel}[^"\\]+)'] |