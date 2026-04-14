# Code Changes for microsoft-evsecurity-xml-ds-object-modify-success-4738 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['attribute', 'channel', 'dest_domain', 'dest_user', 'dest_user_sid', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'new_attribute', 'old_attribute', 'run_level', 'src_domain', 'src_user', 'time', 'uac_status', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |