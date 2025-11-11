# Code Changes for microsoft-evsecurity-kv-group-member-add-success-memberaddedinsecurity (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_user_sid', 'domain', 'event_code', 'event_name', 'group_domain', 'group_id', 'group_name', 'group_type', 'host', 'login_id', 'src_host', 'time', 'user', 'user_dn', 'user_ou'] |
| edit_regex_field | host |  | ['ComputerName=({src_host}({host}[\w.\-]+))'] |
| added_regex_field | src_host |  | ['ComputerName=({src_host}({host}[\w.\-]+))'] |
| removed_attribute | DupFields |  | N/A |