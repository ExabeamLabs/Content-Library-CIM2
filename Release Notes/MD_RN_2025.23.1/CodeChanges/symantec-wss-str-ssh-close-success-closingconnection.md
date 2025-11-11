# Code Changes for symantec-wss-str-ssh-close-success-closingconnection (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | dest_host |  | [' ProxySG: ({event_code}[^\s]+)\s({event_category}SSH)[^:]*:\s*({event_name}Closing connection to (({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({dest_host}[\w.\-]+)))', '({dest_host}[\w.-]+) ProxySG:'] |
| removed_attribute | DupFields |  | N/A |