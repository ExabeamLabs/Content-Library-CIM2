# Code Changes for microsoft-windows-xml-endpoint-notification-success-102 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'dest_host', 'event_code', 'host', 'result', 'run_level', 'task_name', 'time'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |