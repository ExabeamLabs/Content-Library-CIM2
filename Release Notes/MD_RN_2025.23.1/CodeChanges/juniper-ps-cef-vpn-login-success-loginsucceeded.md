# Code Changes for juniper-ps-cef-vpn-login-success-loginsucceeded (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'dest_host', 'dest_ip', 'dest_port', 'host', 'src_host', 'src_ip', 'src_port', 'time', 'user'] |
| added_regex_field | account |  | ['\ssuser=({account}[\w\.\-\!\#\^\~]{1,40}\$?)(\s+\w+=|$)'] |
| added_regex_field | host |  | ['\sdvchost=({host}.+?)(\s+\w+=|$)'] |
| removed_attribute | DupFields |  | N/A |