# Code Changes for unix-dhcpd-csv-dhcp-session-success-dhcpdrenewed (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'dest_ip', 'host', 'process_id', 'process_name', 'user'] |
| edit_regex_field | dest_host |  | ['({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}),Renewed,(|({dest_host}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))'] |
| edit_regex_field | dest_ip |  | ['({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}),Renewed,(|({dest_host}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))'] |
| added_regex_field | user |  | ['({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}),Renewed,(|({dest_host}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))'] |
| removed_attribute | DupFields |  | N/A |