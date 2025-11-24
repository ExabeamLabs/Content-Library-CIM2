# Code Changes for unix-unix-str-user-password-modify-success-chage (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'dest_user', 'host', 'process_id', 'process_name'] |
| edit_regex_field | account |  | ['changed password expiry for ({dest_user}({account}\S+))'] |
| added_regex_field | dest_user |  | ['changed password expiry for ({dest_user}({account}\S+))'] |
| removed_attribute | DupFields |  | N/A |