# Code Changes for windows-events-1 (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'channel', 'event_code', 'event_name', 'group_domain', 'group_id', 'group_name', 'privileges', 'result', 'run_level', 'sid_history', 'time'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |