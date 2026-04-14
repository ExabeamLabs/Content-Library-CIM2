# Code Changes for microsoft-evsecurity-json-ds-object-modify-success-5136 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['activity_id', 'additional_info', 'attribute', 'attribute_value', 'category', 'channel', 'dest_host', 'domain', 'ds_name', 'ds_object_dn', 'ds_type', 'event_code', 'event_name', 'host', 'log_source', 'login_id', 'object_type', 'operation_type', 'process_guid', 'process_id', 'result', 'severity', 'src_domain', 'src_user', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['"+Channel\\?"+:\\?"+({channel}[^"\\]+)', '<Channel>({channel}[^<]+)<\/Channel>'] |