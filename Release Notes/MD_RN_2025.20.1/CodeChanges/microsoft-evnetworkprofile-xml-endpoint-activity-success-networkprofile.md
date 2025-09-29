# Code Changes for microsoft-evnetworkprofile-xml-endpoint-activity-success-networkprofile (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'domain', 'event_code', 'event_id', 'event_name', 'host', 'process_id', 'result', 'run_level', 'service_state', 'task_name', 'thread_id', 'time', 'user', 'user_sid'] |
| removed_regex_field | state |  | [] |
| added_regex_field | service_state |  | ['<Data Name=(\'|")State(\'|")>({service_state}[^<]+)</Data>'] |