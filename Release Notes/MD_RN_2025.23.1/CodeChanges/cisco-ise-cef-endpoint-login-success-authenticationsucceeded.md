# Code Changes for cisco-ise-cef-endpoint-login-success-authenticationsucceeded (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['auth_server', 'computer_name', 'dest_host', 'dest_ip', 'dest_port', 'domain', 'email_address', 'email_domain', 'host', 'location', 'network', 'src_host', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | dest_host |  | ['\Wdhost=({computer_name}({dest_host}[\w\-.]+))'] |
| edit_regex_field | dest_ip |  | ['\Wdst=({auth_server}({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})))(:({dest_port}\d+))?'] |
| edit_regex_field | dest_port |  | ['\Wdst=({auth_server}({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})))(:({dest_port}\d+))?'] |
| added_regex_field | auth_server |  | ['\Wdst=({auth_server}({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})))(:({dest_port}\d+))?'] |
| added_regex_field | computer_name |  | ['\Wdhost=({computer_name}({dest_host}[\w\-.]+))'] |
| removed_attribute | DupFields |  | N/A |