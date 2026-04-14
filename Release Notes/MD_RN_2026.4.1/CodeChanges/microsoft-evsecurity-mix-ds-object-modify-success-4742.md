# Code Changes for microsoft-evsecurity-mix-ds-object-modify-success-4742 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'attribute', 'channel', 'dest_host', 'dest_ip', 'dest_user', 'domain', 'ds_object_dn', 'event_code', 'event_name', 'host', 'login_id', 'new_value', 'old_value', 'src_host', 'src_host_windows', 'time', 'uac_status', 'user'] |
| added_regex_field | channel |  | ['"Channel":"({channel}[^"]+)'] |