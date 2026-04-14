# Code Changes for microsoft-evsecurity-xml-member-remove-success-4762-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_id', 'channel', 'dest_user_sid', 'domain', 'event_code', 'group_domain', 'group_name', 'host', 'login_id', 'member', 'process_guid', 'process_id', 'provider_name', 'result', 'run_level', 'src_domain', 'src_user', 'sub_category', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |