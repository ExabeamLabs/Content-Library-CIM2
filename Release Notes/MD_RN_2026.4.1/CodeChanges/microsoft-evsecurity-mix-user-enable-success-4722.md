# Code Changes for microsoft-evsecurity-mix-user-enable-success-4722 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'dest_domain', 'dest_user', 'domain', 'event_code', 'event_id', 'event_name', 'host', 'login_id', 'time', 'user'] |
| added_regex_field | channel |  | ['"Channel":"({channel}[^"]+)'] |