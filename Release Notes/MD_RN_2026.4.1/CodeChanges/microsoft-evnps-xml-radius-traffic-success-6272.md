# Code Changes for microsoft-evnps-xml-radius-traffic-success-6272 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access_type', 'auth_server', 'auth_type', 'channel', 'dest_ip', 'dest_port', 'domain', 'event_code', 'event_id', 'host', 'location', 'run_level', 'src_domain', 'src_host', 'src_ip', 'src_mac', 'src_port', 'src_user', 'time', 'user', 'user_sid', 'user_type', 'user_upn'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<\/Channel>'] |