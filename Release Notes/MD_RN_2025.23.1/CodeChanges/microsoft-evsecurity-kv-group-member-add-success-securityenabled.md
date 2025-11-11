# Code Changes for microsoft-evsecurity-kv-group-member-add-success-securityenabled (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_domain', 'account_name', 'dest_host', 'dest_user_sid', 'domain', 'event_code', 'event_id', 'event_name', 'group_domain', 'group_id', 'group_name', 'group_type', 'host', 'login_id', 'time', 'user', 'user_dn', 'user_ou'] |
| edit_regex_field | host |  | ['"agent_hostname":"({dest_host}({host}[^"]+))"', '"computer":"({dest_host}({host}[^"]+))"', '(?i)(((audit|success|failure)( |_)(success|audit|failure))|information)(,|\s+)({dest_host}({host}[\w.\-]+))', 'Computer=({dest_host}({host}[\w\-.]+))'] |
| added_regex_field | dest_host |  | ['"agent_hostname":"({dest_host}({host}[^"]+))"', '"computer":"({dest_host}({host}[^"]+))"', '(?i)(((audit|success|failure)( |_)(success|audit|failure))|information)(,|\s+)({dest_host}({host}[\w.\-]+))', 'Computer=({dest_host}({host}[\w\-.]+))'] |
| removed_attribute | DupFields |  | N/A |