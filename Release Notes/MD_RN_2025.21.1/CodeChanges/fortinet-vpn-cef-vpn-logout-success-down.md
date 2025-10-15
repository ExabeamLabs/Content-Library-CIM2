# Code Changes for fortinet-vpn-cef-vpn-logout-success-down (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'action', 'bytes_in', 'bytes_out', 'description', 'dest_host', 'dest_ip', 'devid', 'email_address', 'event_name', 'host', 'host_ip', 'log_uid', 'realm', 'result_reason', 'session_duration', 'severity', 'src_ip', 'src_port', 'src_translated_ip', 'time', 'tz', 'user'] |
| edit_regex_field | host |  | ['({time}\d\d\d\d\/\d\d\/\d\d \d\d:\d\d:\d\d),[^,]*,({dest_ip}({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}))', '\Wdevname="+({dest_host}({host}[\w\-.]+))'] |
| edit_regex_field | host_ip |  | ['\d\d:\d\d:\d\d ({dest_ip}({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})))\b'] |
| edit_regex_field | time |  | ['({time}\d\d\d\d\/\d\d\/\d\d \d\d:\d\d:\d\d),[^,]*,({dest_ip}({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}))', 'date=({time}\d\d\d\d-\d\d-\d\d time=\d\d:\d\d:\d\d([+-]\d\d:\d\d)?)'] |
| edit_regex_field | user |  | ['\Wuser="(.+?\\\\)?(?:N\/A|({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))"'] |
| added_regex_field | account |  | ['\Wuser="(.+?\\\\)?(?:N\/A|({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))"'] |
| added_regex_field | dest_host |  | ['\Wdevname="+({dest_host}({host}[\w\-.]+))'] |
| added_regex_field | dest_ip |  | ['({time}\d\d\d\d\/\d\d\/\d\d \d\d:\d\d:\d\d),[^,]*,({dest_ip}({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}))', '\d\d:\d\d:\d\d ({dest_ip}({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})))\b'] |
| removed_attribute | DupFields |  | N/A |