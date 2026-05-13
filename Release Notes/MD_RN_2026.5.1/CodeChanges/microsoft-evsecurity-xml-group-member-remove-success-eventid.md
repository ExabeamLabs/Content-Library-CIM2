# Code Changes for microsoft-evsecurity-xml-group-member-remove-success-eventid (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_id', 'channel', 'dest_host', 'dest_user', 'dest_user_full_name', 'dest_user_sid', 'domain', 'event_code', 'event_name', 'group_domain', 'group_id', 'group_name', 'group_type', 'host', 'login_id', 'member', 'run_level', 'src_domain', 'src_user', 'time', 'user', 'user_dn', 'user_ou', 'user_sid'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |