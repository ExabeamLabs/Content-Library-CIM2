# Code Changes for microsoft-evsecurity-json-group-member-remove-success-memberremoved-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_domain', 'account_name', 'dest_host', 'dest_user_sid', 'domain', 'event_code', 'event_name', 'group_domain', 'group_id', 'group_name', 'group_type', 'host', 'login_id', 'time', 'user', 'user_dn', 'user_ou'] |
| edit_regex_field | host |  | ['"agent_hostname":"({dest_host}({host}[^"]+))"', '"computer":"({dest_host}({host}[^"]+))"', '(?i)(success|audit)\s+\w+\s+({dest_host}({host}[\w\-.]+))\s'] |
| added_regex_field | dest_host |  | ['"agent_hostname":"({dest_host}({host}[^"]+))"', '"computer":"({dest_host}({host}[^"]+))"', '(?i)(success|audit)\s+\w+\s+({dest_host}({host}[\w\-.]+))\s'] |
| removed_attribute | DupFields |  | N/A |