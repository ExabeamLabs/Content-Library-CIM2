# Code Changes for checkpoint-sg-json-vpn-login-success-ipchanged (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'category', 'dest_ip', 'dest_port', 'email_address', 'event_name', 'full_name', 'origin_ip', 'origin_name', 'rule_type', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | action |  | ['action:"({action}[^",;]+)'] |
| edit_regex_field | event_name |  | ['event_name:"({event_name}[^"]+)', 'om:+"+({event_name}[^",;]+)'] |
| edit_regex_field | src_ip |  | ['src:"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?'] |
| edit_regex_field | src_port |  | ['src:"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?'] |
| removed_regex_field | src_translated_ip |  | [] |
| edit_regex_field | user |  | ['user:"({full_name}[^,:\("]+)\s\((({email_address}([A-Za-z0-9]+[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\)', 'user:+"+CN=(?:[^_]+_)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)'] |
| added_regex_field | category |  | ['cvpn_category:"({category}[^"]+)'] |
| added_regex_field | email_address |  | ['user:"({full_name}[^,:\("]+)\s\((({email_address}([A-Za-z0-9]+[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\)'] |
| added_regex_field | full_name |  | ['user:"({full_name}[^,:\("]+)\s\((({email_address}([A-Za-z0-9]+[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\)'] |
| added_regex_field | origin_ip |  | ['origin:"({origin_ip}[A-Fa-f:\d.]+)'] |
| added_regex_field | origin_name |  | ['origin_?sic_?name:"CN=({origin_name}[^",]+)'] |
| added_regex_field | rule_type |  | ['cu_rule_category:"({rule_type}[^"]+)'] |