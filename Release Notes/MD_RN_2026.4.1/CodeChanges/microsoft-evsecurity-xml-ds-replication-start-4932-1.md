# Code Changes for microsoft-evsecurity-xml-ds-replication-start-4932-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'dest_dc', 'dest_dra', 'event_code', 'host', 'process_id', 'result', 'run_level', 'session_id', 'src_dc', 'src_dra', 'sub_category', 'time'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |