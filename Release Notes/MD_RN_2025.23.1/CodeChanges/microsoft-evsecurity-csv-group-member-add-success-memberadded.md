# Code Changes for microsoft-evsecurity-csv-group-member-add-success-memberadded (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_domain', 'account_name', 'computer_name', 'dest_user_sid', 'domain', 'event_code', 'group_domain', 'group_id', 'group_name', 'group_type', 'host', 'login_id', 'user', 'user_dn'] |
| edit_regex_field | host |  | ['ComputerName=({computer_name}({host}[\w.\-]+))'] |
| added_regex_field | computer_name |  | ['ComputerName=({computer_name}({host}[\w.\-]+))'] |
| removed_attribute | DupFields |  | N/A |