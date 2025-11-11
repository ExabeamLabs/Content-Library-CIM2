# Code Changes for microsoft-evsecurity-kv-audit_policy-modify-success-auditpolicychange (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['domain', 'event_code', 'event_name', 'host', 'login_id', 'policy_name', 'src_host', 'time', 'user'] |
| edit_regex_field | host |  | ['\s+(Information|Audit Success|Success Audit)\s+({src_host}({host}[\w.\-]+))'] |
| added_regex_field | src_host |  | ['\s+(Information|Audit Success|Success Audit)\s+({src_host}({host}[\w.\-]+))'] |
| removed_attribute | DupFields |  | N/A |