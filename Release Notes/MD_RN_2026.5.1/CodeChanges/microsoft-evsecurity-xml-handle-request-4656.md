# Code Changes for microsoft-evsecurity-xml-handle-request-4656 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'channel', 'domain', 'event_code', 'event_name', 'file_dir', 'file_ext', 'file_name', 'file_path', 'handle_id', 'host', 'login_id', 'object', 'object_class', 'object_id', 'object_server', 'object_type', 'operation_type', 'process_dir', 'process_id', 'process_name', 'process_path', 'registry_key', 'registry_path', 'result', 'run_level', 'src_domain', 'src_user', 'time', 'transaction_id', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |