# Code Changes for microsoft-evsecurity-cef-handle-request-success-4656 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'channel', 'dest_host', 'domain', 'event_code', 'event_id', 'event_name', 'handle_id', 'host', 'login_id', 'object', 'object_id', 'object_server', 'object_type', 'operation_type', 'privileges', 'process_id', 'process_path', 'src_domain', 'src_user', 'thread_id', 'time', 'transaction_id', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['"Channel":"({channel}[^"]+)"'] |