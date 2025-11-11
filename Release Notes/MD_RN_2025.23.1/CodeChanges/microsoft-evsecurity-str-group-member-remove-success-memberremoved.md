# Code Changes for microsoft-evsecurity-str-group-member-remove-success-memberremoved (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_domain', 'account_name', 'dest_host', 'dest_user_sid', 'domain', 'event_code', 'event_name', 'group_domain', 'group_id', 'group_name', 'group_type', 'host', 'login_id', 'time', 'user', 'user_dn', 'user_ou'] |
| edit_regex_field | host |  | ['(?i)(success|failure|audit)\s+\w+\s+({dest_host}({host}[\w\-.]+))', 'Computer(\w+)?["\s]*(:|=)\s*"?({dest_host}({host}.+?))("|\s)', 'Information(,|\s+)({dest_host}({host}[\w.\-]+))'] |
| added_regex_field | dest_host |  | ['(?i)(success|failure|audit)\s+\w+\s+({dest_host}({host}[\w\-.]+))', 'Computer(\w+)?["\s]*(:|=)\s*"?({dest_host}({host}.+?))("|\s)', 'Information(,|\s+)({dest_host}({host}[\w.\-]+))'] |
| removed_attribute | DupFields |  | N/A |