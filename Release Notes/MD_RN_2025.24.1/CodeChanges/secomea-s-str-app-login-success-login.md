# Code Changes for secomea-s-str-app-login-success-login (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'domain', 'full_name', 'host', 'operation', 'src_host', 'src_ip', 'time', 'user_id'] |
| edit_regex_field | action |  | ['\s({host}[^\s]+) AUDIT - - - (({domain}\S+)|[^\\]+)\\({user_id}[^\(]+)\s\(({full_name}[^\)]+)?\)\: ({operation}({action}Login))\s'] |
| edit_regex_field | domain |  | ['\s({host}[^\s]+) AUDIT - - - (({domain}\S+)|[^\\]+)\\({user_id}[^\(]+)\s\(({full_name}[^\)]+)?\)\: ({operation}({action}Login))\s'] |
| edit_regex_field | full_name |  | ['\s({host}[^\s]+) AUDIT - - - (({domain}\S+)|[^\\]+)\\({user_id}[^\(]+)\s\(({full_name}[^\)]+)?\)\: ({operation}({action}Login))\s'] |
| edit_regex_field | host |  | ['\s({host}[^\s]+) AUDIT - - - (({domain}\S+)|[^\\]+)\\({user_id}[^\(]+)\s\(({full_name}[^\)]+)?\)\: ({operation}({action}Login))\s'] |
| edit_regex_field | user_id |  | ['\s({host}[^\s]+) AUDIT - - - (({domain}\S+)|[^\\]+)\\({user_id}[^\(]+)\s\(({full_name}[^\)]+)?\)\: ({operation}({action}Login))\s'] |
| added_regex_field | operation |  | ['\s({host}[^\s]+) AUDIT - - - (({domain}\S+)|[^\\]+)\\({user_id}[^\(]+)\s\(({full_name}[^\)]+)?\)\: ({operation}({action}Login))\s'] |
| removed_attribute | DupFields |  | N/A |