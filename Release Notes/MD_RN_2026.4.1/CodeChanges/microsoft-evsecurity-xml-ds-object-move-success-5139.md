# Code Changes for microsoft-evsecurity-xml-ds-object-move-success-5139 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'domain', 'ds_name', 'ds_object_dn', 'ds_type', 'event_code', 'host', 'login_id', 'object_id', 'object_type', 'run_level', 'src_domain', 'src_ds_object_dn', 'src_user', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |