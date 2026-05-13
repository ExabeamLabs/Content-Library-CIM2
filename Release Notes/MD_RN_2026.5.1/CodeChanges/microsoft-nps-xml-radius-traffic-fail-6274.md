# Code Changes for microsoft-nps-xml-radius-traffic-fail-6274 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['auth_server', 'channel', 'dest_ip', 'dest_port', 'domain', 'event_code', 'full_name', 'host', 'location', 'result', 'result_reason', 'run_level', 'src_domain', 'src_user', 'time', 'user', 'user_group_name', 'user_type', 'user_upn'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |