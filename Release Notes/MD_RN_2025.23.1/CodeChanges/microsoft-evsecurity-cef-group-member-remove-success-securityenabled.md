# Code Changes for microsoft-evsecurity-cef-group-member-remove-success-securityenabled (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_id', 'dest_host', 'dest_user_sid', 'domain', 'event_code', 'event_name', 'group_name', 'group_type', 'host', 'login_id', 'time', 'user'] |
| edit_regex_field | host |  | ['shost=({dest_host}({host}[\w\-\.]+))'] |
| added_regex_field | dest_host |  | ['shost=({dest_host}({host}[\w\-\.]+))'] |
| removed_attribute | DupFields |  | N/A |