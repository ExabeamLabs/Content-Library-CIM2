# Code Changes for microsoft-evsecurity-json-group-member-add-success-4756 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_domain', 'account_name', 'category', 'channel', 'dest_user_sid', 'domain', 'event_code', 'group_domain', 'group_id', 'group_name', 'host', 'login_id', 'process_id', 'provider_name', 'time', 'user', 'user_dn', 'user_ou', 'user_sid'] |
| added_regex_field | channel |  | ['"Channel":"({channel}[^"]+)"'] |