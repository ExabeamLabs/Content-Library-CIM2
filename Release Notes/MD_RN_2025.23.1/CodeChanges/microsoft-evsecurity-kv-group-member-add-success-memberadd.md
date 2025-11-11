# Code Changes for microsoft-evsecurity-kv-group-member-add-success-memberadd (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_domain', 'account_id', 'account_name', 'dest_host', 'dest_user_sid', 'domain', 'event_code', 'event_name', 'group_domain', 'group_id', 'group_name', 'group_type', 'host', 'login_id', 'member', 'time', 'user', 'user_dn', 'user_ou'] |
| edit_regex_field | account_id |  | ['Member:\s*Security ID:\s*({member}({account_id}.+?))\s*Account Name:'] |
| edit_regex_field | host |  | ['Computer=({dest_host}({host}[^\s]+))'] |
| added_regex_field | dest_host |  | ['Computer=({dest_host}({host}[^\s]+))'] |
| added_regex_field | member |  | ['Member:\s*Security ID:\s*({member}({account_id}.+?))\s*Account Name:'] |
| removed_attribute | DupFields |  | N/A |