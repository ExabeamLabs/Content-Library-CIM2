# Code Changes for microsoft-evsecurity-json-ds-object-activity-success-4662-3 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'action', 'activity_id', 'additional_info', 'app', 'channel', 'dest_domain', 'dest_login_id', 'dest_user', 'dest_user_sid', 'domain', 'event_code', 'event_id', 'event_name', 'full_name', 'host', 'login_id', 'login_type', 'object', 'object_name', 'object_server', 'object_type', 'operation', 'os', 'privileges', 'process_id', 'provider_name', 'result', 'sid_history', 'src_domain', 'src_host', 'src_user', 'task_name', 'thread_id', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['"channel":"({channel}[^"]+)"'] |