# Code Changes for unix-dhcpd-str-dhcp-session-success-dhcprequest (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'dest_interface', 'dest_ip', 'dest_mac', 'dest_port', 'host', 'user'] |
| edit_regex_field | dest_host |  | ['({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}),Renewed,({dest_host}({user}[\w\.\-\!\#\^\~]{1,40}\$?))', 'from ({dest_mac}[A-Fa-f:\d.]+)( \((?!\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})({dest_host}({user}[\w\.\-\!\#\^\~]{1,40}\$?))\))? via ({dest_interface}[^\s\"]+)'] |
| edit_regex_field | dest_interface |  | ['from ({dest_mac}[A-Fa-f:\d.]+)( \((?!\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})({dest_host}({user}[\w\.\-\!\#\^\~]{1,40}\$?))\))? via ({dest_interface}[^\s\"]+)'] |
| edit_regex_field | dest_ip |  | ['({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}),Renewed,({dest_host}({user}[\w\.\-\!\#\^\~]{1,40}\$?))', 'DHCPREQUEST for ({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?'] |
| edit_regex_field | dest_mac |  | ['from ({dest_mac}[A-Fa-f:\d.]+)( \((?!\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})({dest_host}({user}[\w\.\-\!\#\^\~]{1,40}\$?))\))? via ({dest_interface}[^\s\"]+)'] |
| added_regex_field | user |  | ['({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}),Renewed,({dest_host}({user}[\w\.\-\!\#\^\~]{1,40}\$?))', 'from ({dest_mac}[A-Fa-f:\d.]+)( \((?!\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})({dest_host}({user}[\w\.\-\!\#\^\~]{1,40}\$?))\))? via ({dest_interface}[^\s\"]+)'] |
| removed_attribute | DupFields |  | N/A |