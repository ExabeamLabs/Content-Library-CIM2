# Code Changes for microsoft-evsecurity-cef-user-switch-success-4648 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'dest_host', 'dest_ip', 'dest_port', 'dest_user', 'domain', 'event_code', 'event_name', 'host', 'location', 'login_id', 'process_dir', 'process_name', 'process_path', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | dest_host |  | ['\sdvchost=({host}({dest_host}[\w\-.]+))'] |
| edit_regex_field | dest_ip |  | ['\sdvc=({host}({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})))(:({dest_port}\d+))?'] |
| edit_regex_field | dest_port |  | ['\sdvc=({host}({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})))(:({dest_port}\d+))?'] |
| edit_regex_field | dest_user |  | ['\sduser=({account}({dest_user}.+?))\s+\w+='] |
| added_regex_field | account |  | ['\sduser=({account}({dest_user}.+?))\s+\w+='] |
| added_regex_field | host |  | ['\sdvc=({host}({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})))(:({dest_port}\d+))?', '\sdvchost=({host}({dest_host}[\w\-.]+))'] |
| removed_attribute | DupFields |  | N/A |