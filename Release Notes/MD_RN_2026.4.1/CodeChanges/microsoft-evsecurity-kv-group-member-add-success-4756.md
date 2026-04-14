# Code Changes for microsoft-evsecurity-kv-group-member-add-success-4756 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_domain', 'account_id', 'account_name', 'channel', 'dest_user_sid', 'domain', 'event_code', 'group_domain', 'group_id', 'group_name', 'group_type', 'host', 'login_id', 'time', 'user', 'user_dn', 'user_ou'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |