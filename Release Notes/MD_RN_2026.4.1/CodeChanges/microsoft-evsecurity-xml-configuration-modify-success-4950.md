# Code Changes for microsoft-evsecurity-xml-configuration-modify-success-4950 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'channel', 'dest_host', 'event_code', 'host', 'process_id', 'result', 'run_level', 'thread_id', 'time'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |