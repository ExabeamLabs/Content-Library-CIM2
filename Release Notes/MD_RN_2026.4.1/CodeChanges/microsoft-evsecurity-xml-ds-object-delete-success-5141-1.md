# Code Changes for microsoft-evsecurity-xml-ds-object-delete-success-5141-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'domain', 'ds_object_dn', 'event_code', 'event_name', 'host', 'login_id', 'object_type', 'run_level', 'src_domain', 'src_ip', 'src_port', 'src_user', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['"Channel":"({channel}[^"]+)', '"Channel":"({channel}[^"]+)"'] |