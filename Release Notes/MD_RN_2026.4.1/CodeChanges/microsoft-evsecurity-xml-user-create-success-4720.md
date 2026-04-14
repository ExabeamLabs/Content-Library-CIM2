# Code Changes for microsoft-evsecurity-xml-user-create-success-4720 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_domain', 'account_id', 'account_name', 'channel', 'dest_domain', 'dest_user', 'domain', 'event_code', 'host', 'login_id', 'run_level', 'src_domain', 'src_host', 'src_user', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |