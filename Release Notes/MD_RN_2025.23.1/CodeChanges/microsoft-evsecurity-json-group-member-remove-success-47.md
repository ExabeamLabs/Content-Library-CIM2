# Code Changes for microsoft-evsecurity-json-group-member-remove-success-47 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_domain', 'account_name', 'dest_host', 'dest_user_sid', 'domain', 'event_code', 'event_name', 'group_domain', 'group_id', 'group_name', 'group_type', 'host', 'login_id', 'time', 'user', 'user_dn', 'user_ou'] |
| edit_regex_field | host |  | ['Computer(Name)? = "+({dest_host}({host}[^"]+))"'] |
| added_regex_field | dest_host |  | ['Computer(Name)? = "+({dest_host}({host}[^"]+))"'] |
| removed_attribute | DupFields |  | N/A |