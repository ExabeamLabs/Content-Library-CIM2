# Code Changes for microsoft-evsecurity-mix-audit-policy-modify-success-4719 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['audit_category', 'audit_policy_name', 'channel', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'src_host', 'sub_category', 'time', 'user'] |
| added_regex_field | channel |  | ['"Channel":"({channel}[^"]+)'] |