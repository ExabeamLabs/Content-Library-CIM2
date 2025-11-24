# Code Changes for unix-unix-str-endpoint-login-fail-expiredpassword (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'failure_reason', 'host', 'process_id', 'process_name', 'user'] |
| edit_regex_field | account |  | ['expired password for user ({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)) \(({failure_reason}[^\)]+?)\)'] |
| edit_regex_field | failure_reason |  | ['expired password for user ({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)) \(({failure_reason}[^\)]+?)\)'] |
| added_regex_field | user |  | ['expired password for user ({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)) \(({failure_reason}[^\)]+?)\)'] |
| removed_attribute | DupFields |  | N/A |