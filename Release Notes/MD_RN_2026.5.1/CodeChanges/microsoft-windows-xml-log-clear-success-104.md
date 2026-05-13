# Code Changes for microsoft-windows-xml-log-clear-success-104 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'dest_host', 'dest_ip', 'dest_port', 'domain', 'event_code', 'event_name', 'host', 'result', 'run_level', 'src_domain', 'src_user', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |