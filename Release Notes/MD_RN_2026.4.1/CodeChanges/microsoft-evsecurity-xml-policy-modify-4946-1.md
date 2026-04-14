# Code Changes for microsoft-evsecurity-xml-policy-modify-4946-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['activity_id', 'channel', 'event_code', 'event_id', 'host', 'process_id', 'result', 'rule', 'rule_id', 'run_level', 'thread_id', 'time'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |