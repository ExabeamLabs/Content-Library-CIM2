# Code Changes for azure-ad-system-info (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['activity_id', 'channel', 'event_code', 'event_name', 'process_id', 'result', 'run_level', 'thread_id', 'time', 'user_sid'] |
| added_regex_field | activity_id |  | ['<Correlation ActivityID\\*=(\'|")\{({activity_id}[^\}\'"]+)'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<\/Channel>'] |
| added_regex_field | event_code |  | ['<EventID>({event_code}\d+)</EventID>'] |
| added_regex_field | process_id |  | ['<Execution ProcessID=(\'|")({process_id}\d+)(\'|") ThreadID=(\'|")({thread_id}\d+)'] |
| added_regex_field | thread_id |  | ['<Execution ProcessID=(\'|")({process_id}\d+)(\'|") ThreadID=(\'|")({thread_id}\d+)'] |