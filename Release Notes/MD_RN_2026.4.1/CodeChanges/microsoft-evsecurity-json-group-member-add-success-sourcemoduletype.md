# Code Changes for microsoft-evsecurity-json-group-member-add-success-sourcemoduletype (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_id', 'channel', 'dest_host', 'dest_user_sid', 'domain', 'event_code', 'event_id', 'event_name', 'group_domain', 'group_name', 'group_type', 'host', 'login_id', 'member', 'src_domain', 'src_user', 'time', 'user', 'user_dn', 'user_ou', 'user_sid'] |
| added_regex_field | channel |  | ['"Channel":"({channel}[^"]+)"'] |