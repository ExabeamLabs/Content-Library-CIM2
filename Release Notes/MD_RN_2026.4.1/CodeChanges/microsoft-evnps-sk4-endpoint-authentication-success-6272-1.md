# Code Changes for microsoft-evnps-sk4-endpoint-authentication-success-6272-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['auth_server', 'auth_type', 'channel', 'dest_ip', 'dest_port', 'domain', 'event_code', 'event_name', 'host', 'log_source', 'login_id', 'src_domain', 'src_host', 'src_ip', 'src_mac', 'src_port', 'src_user', 'time', 'user', 'user_sid', 'user_type', 'user_upn'] |
| added_regex_field | channel |  | ['"Channel":"({channel}[^"]+)', 'Channel"?(:|=)"?({channel}[^"<]+)'] |