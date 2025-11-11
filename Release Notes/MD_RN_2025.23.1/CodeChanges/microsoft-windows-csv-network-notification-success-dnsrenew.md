# Code Changes for microsoft-windows-csv-network-notification-success-dnsrenew (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'dest_ip', 'dest_mac', 'host', 'time', 'user'] |
| edit_regex_field | dest_host |  | [',(解放|期限切れ),({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}),({dest_host}({user}[\w\.\-\!\#\^\~]{1,40}\$?))?,({dest_mac}[^,]+)?,'] |
| edit_regex_field | dest_ip |  | [',(解放|期限切れ),({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}),({dest_host}({user}[\w\.\-\!\#\^\~]{1,40}\$?))?,({dest_mac}[^,]+)?,'] |
| edit_regex_field | dest_mac |  | [',(解放|期限切れ),({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}),({dest_host}({user}[\w\.\-\!\#\^\~]{1,40}\$?))?,({dest_mac}[^,]+)?,'] |
| added_regex_field | user |  | [',(解放|期限切れ),({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}),({dest_host}({user}[\w\.\-\!\#\^\~]{1,40}\$?))?,({dest_mac}[^,]+)?,'] |
| removed_attribute | DupFields |  | N/A |