# Code Changes for microsoft-evsecurity-kv-group-member-remove-success-groupmemberremoved (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_id', 'dest_host', 'dest_user_sid', 'domain', 'event_code', 'event_name', 'group_domain', 'group_id', 'group_name', 'group_type', 'host', 'login_id', 'time', 'user', 'user_dn', 'user_ou'] |
| edit_regex_field | host |  | ['(?:Success|Failure|Audit)\s+\w+\s+({dest_host}({host}[^\s]+))', 'Information\s+({dest_host}({host}[\w.\-]+))\s+'] |
| added_regex_field | dest_host |  | ['(?:Success|Failure|Audit)\s+\w+\s+({dest_host}({host}[^\s]+))', 'Information\s+({dest_host}({host}[\w.\-]+))\s+'] |
| removed_attribute | DupFields |  | N/A |