# Code Changes for microsoft-evsecurity-xml-user-delete-success-4743 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_name', 'channel', 'dest_user', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'object_dn', 'run_level', 'src_host', 'time', 'user'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |