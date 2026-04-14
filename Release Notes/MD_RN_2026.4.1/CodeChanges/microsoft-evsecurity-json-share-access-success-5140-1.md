# Code Changes for microsoft-evsecurity-json-share-access-success-5140-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'action', 'app', 'channel', 'dest_domain', 'dest_host', 'dest_login_id', 'dest_user', 'dest_user_sid', 'domain', 'event_code', 'event_id', 'event_name', 'file_type', 'host', 'login_id', 'login_type', 'operation_id', 'os', 'privileges', 'process_id', 'provider_name', 'result', 'share_name', 'sid_history', 'src_domain', 'src_host', 'src_port', 'src_user', 'task_name', 'thread_id', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['"Channel":"({channel}[^"]+)', '<Channel>({channel}[^<]+)<'] |