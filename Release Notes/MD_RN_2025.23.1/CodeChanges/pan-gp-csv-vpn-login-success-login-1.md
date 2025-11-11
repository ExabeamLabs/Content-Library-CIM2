# Code Changes for pan-gp-csv-vpn-login-success-login-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['device_name', 'domain', 'email_address', 'firewall', 'full_name', 'host', 'serial_num', 'src_ip', 'time', 'user'] |
| edit_regex_field | device_name |  | [',USERID,login,([^,]*,){20}({firewall}({device_name}({host}[^,]+)))'] |
| edit_regex_field | host |  | [',USERID,login,([^,]*,){20}({firewall}({device_name}({host}[^,]+)))'] |
| added_regex_field | firewall |  | [',USERID,login,([^,]*,){20}({firewall}({device_name}({host}[^,]+)))'] |