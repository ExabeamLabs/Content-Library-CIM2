# Code Changes for microsoft-nps-xml-radius-traffic-success-6278 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access_type', 'auth_server', 'auth_type', 'channel', 'dest_ip', 'dest_port', 'domain', 'event_code', 'first_name', 'full_name', 'host', 'last_name', 'location', 'run_level', 'src_domain', 'src_host', 'src_mac', 'src_user', 'time', 'user', 'user_type', 'user_upn'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |