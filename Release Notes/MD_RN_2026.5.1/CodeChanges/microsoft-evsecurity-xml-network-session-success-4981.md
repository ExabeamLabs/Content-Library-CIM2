# Code Changes for microsoft-evsecurity-xml-network-session-success-4981 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'channel', 'dest_host', 'dest_ip', 'dest_port', 'duration', 'event_code', 'host', 'process_id', 'run_level', 'src_host', 'src_ip', 'src_port', 'task_name', 'time'] |
| edit_regex_field | host |  | ['<Computer>({host}[^<]+)', "<\d'+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)'"] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |