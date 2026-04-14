# Code Changes for microsoft-evsecurity-kv-audit-policy-modify-4907 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'account_domain', 'audit_policy_name', 'channel', 'domain', 'event_code', 'event_name', 'handle_id', 'host', 'login_id', 'object', 'object_server', 'object_type', 'process_dir', 'process_id', 'process_name', 'process_path', 'time', 'user'] |
| added_regex_field | channel |  | ['"Channel":"({channel}[^"]+)'] |