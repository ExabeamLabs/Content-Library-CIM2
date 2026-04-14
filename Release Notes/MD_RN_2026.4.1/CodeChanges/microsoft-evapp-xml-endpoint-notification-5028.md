# Code Changes for microsoft-evapp-xml-endpoint-notification-5028 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'dest_host', 'event_code', 'event_id', 'event_name', 'file_dir', 'file_ext', 'file_hash', 'file_name', 'file_path', 'host', 'process_id', 'provider_name', 'result', 'run_level', 'thread_id', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |