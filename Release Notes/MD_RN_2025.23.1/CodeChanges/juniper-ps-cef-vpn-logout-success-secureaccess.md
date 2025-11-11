# Code Changes for juniper-ps-cef-vpn-logout-success-secureaccess (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'dest_ip', 'dest_port', 'email_address', 'full_name', 'host', 'result', 'src_ip', 'src_port', 'src_translated_ip', 'time', 'user'] |
| added_regex_field | account |  | ['\ssuser=({account}[\w\.\-\!\#\^\~]{1,40}\$?)\s+(\w+=|$)'] |
| removed_attribute | DupFields |  | N/A |