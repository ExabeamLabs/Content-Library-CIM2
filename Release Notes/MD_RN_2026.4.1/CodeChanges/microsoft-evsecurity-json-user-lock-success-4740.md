# Code Changes for microsoft-evsecurity-json-user-lock-success-4740 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'event_code', 'event_name', 'host', 'login_id', 'src_domain', 'src_host', 'src_ip', 'src_user', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['"Channel\\?":\\?"({channel}[^"\\]+)'] |