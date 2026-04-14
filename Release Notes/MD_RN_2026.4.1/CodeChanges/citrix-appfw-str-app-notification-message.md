# Code Changes for citrix-appfw-str-app-notification-message (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_attribute | Product |  | Citrix Gateway |
| COULD_NOT_COMPARE | TimeFormat |  | ['MM/dd/yyyy:HH:mm:ss', "yyyy-MM-dd'T'HH:mm:ssZ"] |
| changed | Conditions |  | [' : ', ' default', '-PPE'] |
| changed_parsed_fields | N/A |  | ['additional_info', 'bytes_in', 'bytes_out', 'dest_ip', 'dest_port', 'host', 'protocol', 'session_id', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | host |  | ['({time}\d\d\/\d\d\/\d\d\d\d:\d\d:\d\d:\d\d)(\s+GMT)?\s*({host}[^\s]+).*?:\sdefault\s({protocol}[^\s]+)', '({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\dZ)\s*({host}[^\s]+)\s({protocol}[^\s]+)'] |
| edit_regex_field | protocol |  | ['({time}\d\d\/\d\d\/\d\d\d\d:\d\d:\d\d:\d\d)(\s+GMT)?\s*({host}[^\s]+).*?:\sdefault\s({protocol}[^\s]+)', '({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\dZ)\s*({host}[^\s]+)\s({protocol}[^\s]+)'] |
| edit_regex_field | time |  | ['({time}\d\d\/\d\d\/\d\d\d\d:\d\d:\d\d:\d\d)(\s+GMT)?\s*({host}[^\s]+).*?:\sdefault\s({protocol}[^\s]+)', '({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\dZ)\s*({host}[^\s]+)\s({protocol}[^\s]+)'] |
| added_regex_field | bytes_in |  | ['clientside_rxbytes ({bytes_in}\d+)'] |
| added_regex_field | bytes_out |  | ['clientside_txbytes ({bytes_out}\d+)'] |
| added_regex_field | dest_ip |  | ['gateway_vip ({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?'] |
| added_regex_field | dest_port |  | ['gateway_vip ({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?'] |
| added_regex_field | session_id |  | ['ICAUUID = ({session_id}[^\s\]]+)'] |
| added_regex_field | src_ip |  | ['Remote ip = ({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?'] |
| added_regex_field | src_port |  | ['Remote ip = ({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?'] |
| added_regex_field | user |  | ['Username = ({user}[\w\.\-\!\#\^\~]{1,40}\$?)'] |