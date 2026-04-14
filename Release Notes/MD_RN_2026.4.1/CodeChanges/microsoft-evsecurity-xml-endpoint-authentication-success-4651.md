# Code Changes for microsoft-evsecurity-xml-endpoint-authentication-success-4651 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'dest_host', 'event_code', 'event_name', 'host', 'result', 'run_level', 'src_host', 'task_name', 'time'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |