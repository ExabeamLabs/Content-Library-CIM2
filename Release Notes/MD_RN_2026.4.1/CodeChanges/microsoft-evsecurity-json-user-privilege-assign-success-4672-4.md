# Code Changes for microsoft-evsecurity-json-user-privilege-assign-success-4672-4 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'privileges', 'time', 'user'] |
| added_regex_field | channel |  | ['"Channel":"({channel}[^"]+)'] |