# Code Changes for microsoft-evsecurity-json-audit-policy-modify-4907 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['audit_policy_name', 'channel', 'domain', 'event_code', 'event_name', 'handle_id', 'host', 'login_id', 'object', 'object_server', 'object_type', 'process_dir', 'process_id', 'process_name', 'process_path', 'src_domain', 'src_user', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['"Channel":"({channel}[^"]+)"'] |