# Code Changes for microsoft-evsecurity-xml-handle-close-4658 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'domain', 'event_code', 'host', 'login_id', 'object_id', 'object_server', 'process_dir', 'process_id', 'process_name', 'process_path', 'run_level', 'src_domain', 'src_user', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |