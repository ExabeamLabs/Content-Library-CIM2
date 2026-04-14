# Code Changes for microsoft-nps-sk4-endpoint-authentication-fail-6273 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['auth_server', 'channel', 'dest_ip', 'dest_port', 'domain', 'email_address', 'email_domain', 'event_code', 'event_name', 'failure_reason', 'host', 'location', 'log_source', 'login_id', 'src_domain', 'src_host', 'src_ip', 'src_port', 'src_user', 'time', 'user', 'user_sid', 'user_type'] |
| added_regex_field | channel |  | ['"Channel":"({channel}[^"]+)', 'Channel"?(:|=)"?({channel}[^"<]+)'] |