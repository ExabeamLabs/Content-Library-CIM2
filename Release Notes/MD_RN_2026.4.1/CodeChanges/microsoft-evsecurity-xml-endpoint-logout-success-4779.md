# Code Changes for microsoft-evsecurity-xml-endpoint-logout-success-4779 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'dest_host', 'domain', 'event_code', 'event_id', 'event_name', 'host', 'login_id', 'result', 'run_level', 'src_host', 'src_ip', 'src_port', 'time', 'user'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |