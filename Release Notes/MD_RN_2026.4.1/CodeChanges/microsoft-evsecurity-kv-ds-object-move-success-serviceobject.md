# Code Changes for microsoft-evsecurity-kv-ds-object-move-success-serviceobject (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'correlation_id', 'domain', 'ds_name', 'ds_object_dn', 'ds_type', 'event_code', 'event_name', 'host', 'login_id', 'new_attribute', 'object_id', 'object_type', 'old_attribute', 'src_ds_object_dn', 'src_ds_object_ou', 'src_host', 'src_ip', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['"Channel":"({channel}[^"]+)', '<Channel>({channel}[^<]+)<'] |