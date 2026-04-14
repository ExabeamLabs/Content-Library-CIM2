# Code Changes for microsoft-evsecurity-cef-ds-object-activity-success-4742 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'dest_host', 'dest_user', 'domain', 'ds_object_dn', 'event_code', 'event_id', 'event_name', 'host', 'login_id', 'new_value', 'object_name', 'old_value', 'result', 'src_domain', 'src_user', 'time', 'uac_status', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['"channel":"({channel}[^"]+)"'] |