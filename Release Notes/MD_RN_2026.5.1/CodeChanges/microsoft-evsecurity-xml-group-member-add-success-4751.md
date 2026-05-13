# Code Changes for microsoft-evsecurity-xml-group-member-add-success-4751 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_id', 'channel', 'dest_host', 'domain', 'event_code', 'group_domain', 'group_id', 'group_name', 'host', 'login_id', 'member', 'process_guid', 'process_id', 'run_level', 'src_domain', 'src_user', 'time', 'user', 'user_dn', 'user_ou', 'user_sid'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |