# Code Changes for microsoft-evsecurity-mix-user-password-modify-4723 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'dest_domain', 'dest_user', 'dest_user_sid', 'domain', 'event_code', 'event_id', 'event_name', 'host', 'login_id', 'result', 'src_domain', 'src_host', 'src_ip', 'src_port', 'src_user', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['"Channel":"({channel}[^"]+)'] |