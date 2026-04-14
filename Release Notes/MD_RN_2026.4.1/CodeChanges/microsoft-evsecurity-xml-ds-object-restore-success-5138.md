# Code Changes for microsoft-evsecurity-xml-ds-object-restore-success-5138 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'correlation_id', 'dest_host', 'dest_ip', 'domain', 'ds_name', 'ds_object_dn', 'ds_object_ou', 'ds_type', 'event_code', 'event_name', 'host', 'login_id', 'new_attribute', 'object_id', 'object_type', 'old_attribute', 'run_level', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |