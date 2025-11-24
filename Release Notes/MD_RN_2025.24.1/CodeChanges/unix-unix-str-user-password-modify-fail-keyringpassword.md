# Code Changes for unix-unix-str-user-password-modify-fail-keyringpassword (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'dest_user', 'failure_reason', 'host', 'host_ip', 'process_id', 'process_name', 'time'] |
| edit_regex_field | account |  | ["couldn't update the '({dest_user}({account}[^']+))"] |
| added_regex_field | dest_user |  | ["couldn't update the '({dest_user}({account}[^']+))"] |
| removed_attribute | DupFields |  | N/A |