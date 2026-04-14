# Code Changes for checkpoint-ngfw-cef-endpoint-login-success-identity-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_attribute | TimeFormat |  | epoch_sec |
| changed_parsed_fields | N/A |  | ['auth_method', 'dest_ip', 'dest_port', 'direction', 'domain', 'email_address', 'failure_reason', 'first_name', 'full_name', 'host', 'last_name', 'origin_ip', 'origin_name', 'os', 'product_name', 'result', 'src_host', 'src_ip', 'src_port', 'time', 'user'] |
| removed_regex_field | action |  | [] |
| removed_regex_field | alert_severity |  | [] |
| removed_regex_field | bytes |  | [] |
| removed_regex_field | bytes_in |  | [] |
| removed_regex_field | bytes_out |  | [] |
| removed_regex_field | company |  | [] |
| removed_regex_field | department |  | [] |
| edit_regex_field | dest_ip |  | ['\Wendpoint_ip:"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?', 'host_ip:"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?'] |
| edit_regex_field | dest_port |  | ['\Wendpoint_ip:"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?', 'host_ip:"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?'] |
| removed_regex_field | dest_translated_ip |  | [] |
| edit_regex_field | direction |  | ['ifdir:"({direction}[^"]+)'] |
| edit_regex_field | domain |  | ['\Wdomain_name:"({domain}[^"]+)', '\Wuser:"(-|({email_address}[^@"\s]+@[^@"\s]+)|((({domain}[^\s]+?)[\\]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)))"'] |
| edit_regex_field | email_address |  | ['\Wuser:"(-|({email_address}[^@"\s]+@[^@"\s]+)|((({domain}[^\s]+?)[\\]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)))"', '\Wuser:"({full_name}[^,:\("]+)\s\((({email_address}([A-Za-z0-9]+[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\)'] |
| edit_regex_field | first_name |  | ['\Wuser:"({last_name}[^,]+),\s*({first_name}[\w\s]+\S)\s*\(({user}[\w\.\-\!\#\^\~]{1,40}\$?)\)'] |
| edit_regex_field | full_name |  | ['\Wuser:"({full_name}[^,:\("]+)\s\((({email_address}([A-Za-z0-9]+[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\)'] |
| edit_regex_field | host |  | ['\W({host}[\w\-.]+) CheckPoint'] |
| edit_regex_field | last_name |  | ['\Wuser:"({last_name}[^,]+),\s*({first_name}[\w\s]+\S)\s*\(({user}[\w\.\-\!\#\^\~]{1,40}\$?)\)'] |
| edit_regex_field | origin_ip |  | ['\Worigin:"({origin_ip}[^"]+)'] |
| edit_regex_field | os |  | ['\Wos_name:"({os}[^"]+)"'] |
| edit_regex_field | product_name |  | ['\Wproduct:"({product_name}[^"]+)'] |
| removed_regex_field | protocol |  | [] |
| edit_regex_field | result |  | ['\Wauth_status:"({result}[^"]+)', '\sstatus:"({result}[^"]+)'] |
| removed_regex_field | rule |  | [] |
| edit_regex_field | src_host |  | ['\Wsrc_machine_name:"({src_host}[\w\-.]+)'] |
| removed_regex_field | src_interface |  | [] |
| edit_regex_field | src_ip |  | ['\Wsrc:"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?'] |
| edit_regex_field | src_port |  | ['\Wsrc:"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?'] |
| removed_regex_field | src_translated_ip |  | [] |
| edit_regex_field | time |  | ['\Wtime:"({time}\d{10})'] |
| removed_regex_field | tunnel_protocol |  | [] |
| edit_regex_field | user |  | ['\Wuser:"(-|({email_address}[^@"\s]+@[^@"\s]+)|((({domain}[^\s]+?)[\\]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)))"', '\Wuser:"({full_name}[^,:\("]+)\s\((({email_address}([A-Za-z0-9]+[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\)', '\Wuser:"({last_name}[^,]+),\s*({first_name}[\w\s]+\S)\s*\(({user}[\w\.\-\!\#\^\~]{1,40}\$?)\)'] |
| removed_regex_field | user_ou |  | [] |
| added_regex_field | auth_method |  | ['\Wauth_method:"({auth_method}[^"]+)'] |
| added_regex_field | failure_reason |  | ['reason:"({failure_reason}[^"]+)'] |
| added_regex_field | origin_name |  | ['\Worigin_sic_name:"CN=({origin_name}[^",]+)', 'originsicname:"CN=({origin_name}[^",]+)'] |