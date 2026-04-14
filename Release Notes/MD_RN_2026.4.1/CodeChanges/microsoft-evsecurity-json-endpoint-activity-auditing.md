# Code Changes for microsoft-evsecurity-json-endpoint-activity-auditing (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'new_value', 'old_value', 'process_dir', 'process_id', 'process_name', 'process_path', 'severity', 'src_domain', 'src_user', 'time', 'transaction_id', 'uac_status', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['"Channel":"({channel}[^"]+)"'] |