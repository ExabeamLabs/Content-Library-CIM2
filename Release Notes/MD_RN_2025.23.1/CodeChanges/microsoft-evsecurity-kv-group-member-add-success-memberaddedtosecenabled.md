# Code Changes for microsoft-evsecurity-kv-group-member-add-success-memberaddedtosecenabled (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_id', 'dest_host', 'domain', 'event_code', 'event_name', 'group_name', 'group_type', 'host', 'login_id', 'time', 'user', 'user_dn'] |
| edit_regex_field | host |  | ['shost=({dest_host}({host}[\w\-\.]+))'] |
| added_regex_field | dest_host |  | ['shost=({dest_host}({host}[\w\-\.]+))'] |
| removed_attribute | DupFields |  | N/A |