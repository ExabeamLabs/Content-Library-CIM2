# Code Changes for microsoft-evsecurity-json-endpoint-notification-4611 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['activity_id', 'additional_info', 'category', 'channel', 'event_code', 'event_name', 'host', 'log_source', 'login_id', 'process_id', 'process_name', 'result', 'src_user', 'thread_id', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['"Channel":"({channel}[^"]+)"'] |