# Code Changes for microsoft-evsecurity-kv-endpoint-create-created (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_id', 'attribute', 'channel', 'dest_host', 'dest_user', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'object_dn', 'time', 'user'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |