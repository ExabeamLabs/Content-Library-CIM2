# Code Changes for microsoft-evsecurity-kv-handle-request-4656-2 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'channel', 'dest_host', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'object', 'object_class', 'object_id', 'object_server', 'operation_type', 'privileges', 'process_dir', 'process_id', 'process_name', 'process_path', 'time', 'transaction_id', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['Channel"?(:|>)"?({channel}[^"<]+)'] |