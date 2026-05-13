# Code Changes for microsoft-evsecurity-xml-policy-modify-5447 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'channel', 'domain', 'event_category', 'event_code', 'host', 'process_id', 'provider_name', 'result', 'run_level', 'task_name', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |