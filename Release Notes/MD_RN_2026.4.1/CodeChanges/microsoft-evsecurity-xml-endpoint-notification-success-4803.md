# Code Changes for microsoft-evsecurity-xml-endpoint-notification-success-4803 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'dest_domain', 'dest_login_id', 'dest_user', 'domain', 'event_code', 'host', 'login_id', 'run_level', 'time', 'user'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |