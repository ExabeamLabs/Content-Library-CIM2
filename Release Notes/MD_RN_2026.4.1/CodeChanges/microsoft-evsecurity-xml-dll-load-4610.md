# Code Changes for microsoft-evsecurity-xml-dll-load-4610 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['auth_package', 'channel', 'event_code', 'event_name', 'file_dir', 'file_name', 'file_path', 'host', 'process_id', 'result', 'run_level', 'src_host', 'thread_id', 'time'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |