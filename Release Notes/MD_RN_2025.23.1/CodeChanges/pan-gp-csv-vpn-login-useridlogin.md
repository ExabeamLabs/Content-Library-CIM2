# Code Changes for pan-gp-csv-vpn-login-useridlogin (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['app', 'device_name', 'domain', 'email_address', 'firewall', 'full_name', 'host', 'result_code', 'src_ip', 'time', 'user'] |
| added_regex_field | device_name |  | [',USERID,login,([^,]*,){20}(0|({device_name}({firewall}[^,]+))),'] |
| added_regex_field | firewall |  | [',USERID,login,([^,]*,){20}(0|({device_name}({firewall}[^,]+))),'] |