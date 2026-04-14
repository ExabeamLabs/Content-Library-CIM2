# Code Changes for microsoft-evsecurity-json-handle-copy-4690 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'dest_host', 'dest_process_id', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'process_id', 'result', 'src_domain', 'src_user', 'thread_id', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['"Channel":"({channel}[^"]+)"'] |