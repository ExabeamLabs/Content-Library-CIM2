# Code Changes for microsoft-evossh-xml-ssh-traffic-4 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'channel', 'dest_host', 'event_code', 'host', 'operation', 'result', 'run_level', 'src_ip', 'src_port', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |