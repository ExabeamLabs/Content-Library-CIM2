# Code Changes for microsoft-evsecurity-xml-ds-replication-modify-4931 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'dest_dra', 'event_code', 'event_id', 'host', 'process_guid', 'process_id', 'provider_name', 'result', 'run_level', 'src_dra', 'sub_category', 'thread_id', 'time'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |