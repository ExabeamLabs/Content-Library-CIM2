# Code Changes for unix-unix-str-user-password-expire-success-account (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'event_name', 'failure_reason', 'host', 'user'] |
| edit_regex_field | account |  | ['expired password for user ({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)) \(({failure_reason}[^\)]+?)\)'] |
| edit_regex_field | failure_reason |  | ['expired password for user ({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)) \(({failure_reason}[^\)]+?)\)'] |
| added_regex_field | user |  | ['expired password for user ({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)) \(({failure_reason}[^\)]+?)\)'] |
| removed_attribute | DupFields |  | N/A |