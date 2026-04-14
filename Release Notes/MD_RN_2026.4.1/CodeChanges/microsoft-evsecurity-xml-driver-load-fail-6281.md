# Code Changes for microsoft-evsecurity-xml-driver-load-fail-6281 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'channel', 'event_code', 'file_dir', 'file_ext', 'file_name', 'file_path', 'process_guid', 'process_id', 'result', 'run_level', 'src_host', 'thread_id', 'time'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |