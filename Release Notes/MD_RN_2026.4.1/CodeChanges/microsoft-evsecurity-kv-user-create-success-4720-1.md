# Code Changes for microsoft-evsecurity-kv-user-create-success-4720-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_domain', 'account_id', 'account_name', 'channel', 'dest_domain', 'dest_user', 'domain', 'event_code', 'event_id', 'event_name', 'host', 'login_id', 'time', 'user', 'user_sid', 'user_type'] |
| added_regex_field | channel |  | ['"Channel":"({channel}[^"]+)'] |