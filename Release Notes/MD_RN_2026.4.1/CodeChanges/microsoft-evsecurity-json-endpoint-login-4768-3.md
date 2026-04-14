# Code Changes for microsoft-evsecurity-json-endpoint-login-4768-3 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_domain', 'action', 'activity_id', 'app', 'channel', 'dest_domain', 'dest_user', 'dest_user_sid', 'domain', 'event_code', 'event_id', 'event_name', 'failure_code', 'host', 'key_name', 'key_type', 'login_id', 'login_type', 'operation', 'os', 'privileges', 'process_id', 'provider_name', 'result', 'result_code', 'sid_history', 'src_domain', 'src_host', 'src_ip', 'src_port', 'src_user', 'task_name', 'thread_id', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['"channel\\?"+:\\?"+({channel}[^"\\]+)'] |