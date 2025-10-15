# Code Changes for fortinet-vpn-kv-vpn-login-success-ssl (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'bytes_in', 'bytes_out', 'dest_host', 'dest_ip', 'email_address', 'event_name', 'host', 'realm', 'src_ip', 'src_port', 'src_translated_ip', 'time', 'tz', 'user'] |
| edit_regex_field | host |  | ['({time}\d\d\d\d\/\d\d\/\d\d \d\d:\d\d:\d\d),[^,]*,({dest_ip}({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}))', '\Wdevname="*({dest_host}({host}[\w\-.]+))'] |
| edit_regex_field | time |  | ['({time}\d\d\d\d\/\d\d\/\d\d \d\d:\d\d:\d\d),[^,]*,({dest_ip}({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}))', 'date=({time}\d\d\d\d-\d\d-\d\d time=\d\d:\d\d:\d\d([+-]\d\d:\d\d)?)'] |
| edit_regex_field | user |  | ['\Wuser="(.+?\\\\)?(?:N\/A|({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))"'] |
| added_regex_field | account |  | ['\Wuser="(.+?\\\\)?(?:N\/A|({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))"'] |
| added_regex_field | dest_host |  | ['\Wdevname="*({dest_host}({host}[\w\-.]+))'] |
| added_regex_field | dest_ip |  | ['({time}\d\d\d\d\/\d\d\/\d\d \d\d:\d\d:\d\d),[^,]*,({dest_ip}({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}))'] |
| removed_attribute | DupFields |  | N/A |