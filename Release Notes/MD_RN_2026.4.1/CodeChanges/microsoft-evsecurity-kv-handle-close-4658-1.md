# Code Changes for microsoft-evsecurity-kv-handle-close-4658-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'dest_host', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'object_id', 'object_server', 'operation_type', 'process_dir', 'process_id', 'process_name', 'process_path', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |