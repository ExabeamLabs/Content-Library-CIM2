# Code Changes for microsoft-evsecurity-cef-group-member-add-success-groupmemberadded (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'domain', 'event_code', 'event_name', 'group_domain', 'group_id', 'group_name', 'group_type', 'host', 'login_id', 'time', 'user', 'user_dn', 'user_ou'] |
| edit_regex_field | host |  | ['\sdvchost=({dest_host}({host}[^\s]+))'] |
| added_regex_field | dest_host |  | ['\sdvchost=({dest_host}({host}[^\s]+))'] |
| removed_attribute | DupFields |  | N/A |