# Code Changes for microsoft-evsecurity-xml-network-notfication-4816-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'dest_host', 'event_code', 'event_name', 'host', 'process_guid', 'process_id', 'run_level', 'src_ip', 'src_port', 'thread_id', 'time'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |