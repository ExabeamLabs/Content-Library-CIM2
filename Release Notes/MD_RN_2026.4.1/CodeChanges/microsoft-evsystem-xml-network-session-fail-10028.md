# Code Changes for microsoft-evsystem-xml-network-session-fail-10028 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'channel', 'dest_ip', 'dest_port', 'event_code', 'host', 'process_dir', 'process_id', 'process_name', 'process_path', 'result', 'run_level', 'thread_id', 'time', 'user_sid'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |