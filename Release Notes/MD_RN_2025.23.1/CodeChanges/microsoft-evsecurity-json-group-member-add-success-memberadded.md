# Code Changes for microsoft-evsecurity-json-group-member-add-success-memberadded (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_id', 'dest_host', 'domain', 'event_code', 'event_name', 'group_domain', 'group_name', 'group_type', 'host', 'login_id', 'time', 'user', 'user_dn', 'user_ou', 'user_sid'] |
| edit_regex_field | host |  | ['"MachineName":"({dest_host}({host}[\w\-.]+))'] |
| added_regex_field | dest_host |  | ['"MachineName":"({dest_host}({host}[\w\-.]+))'] |
| removed_attribute | DupFields |  | N/A |