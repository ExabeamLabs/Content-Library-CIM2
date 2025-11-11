# Code Changes for symantec-wss-str-ssh-start-fail-connecttohost (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | dest_host |  | ['({dest_host}[\w.-]+) ProxySG:', 'connect to host (({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[\w.\-]+))\s'] |
| removed_attribute | DupFields |  | N/A |