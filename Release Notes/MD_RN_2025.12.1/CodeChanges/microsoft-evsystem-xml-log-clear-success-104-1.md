# Code Changes for microsoft-evsystem-xml-log-clear-success-104-1 (Parser)

| Code Change | Field Name | 2025.11.1 | 2025.12.1 |
|-------------|------------|-----------|------------|
| changed_parsed_fields | N/A | ['alert_severity', 'channel', 'dest_host', 'dest_ip', 'dest_port', 'domain', 'event_code', 'event_name', 'host', 'process_id', 'result', 'run_level', 'thread_id', 'time', 'user', 'user_sid'] | ['alert_severity', 'channel', 'channel_name', 'dest_host', 'dest_ip', 'dest_port', 'domain', 'event_code', 'event_name', 'host', 'process_id', 'result', 'run_level', 'thread_id', 'time', 'user', 'user_sid'] |
| added_regex_field | channel_name | [] | ['<UserData>.+?<Channel>({channel_name}[^<]+)'] |