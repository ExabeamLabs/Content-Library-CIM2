# Code Changes for microsoft-evsecurity-json-user-privilege-assign-success-4672-6 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'privileges', 'result', 'src_domain', 'src_host', 'src_user', 'time', 'user'] |
| added_regex_field | channel |  | ['"channel":"({channel}[^"]+)'] |