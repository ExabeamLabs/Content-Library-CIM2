# Code Changes for citrix-cgateway-cef-vpn-login-success-login (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'dest_host', 'dest_ip', 'dest_port', 'host', 'realm', 'session_id', 'src_host', 'src_ip', 'src_port', 'src_translated_ip', 'time', 'user', 'user_agent', 'vpn_client_type'] |
| added_regex_field | account |  | ['\s(s|d)user=({account}[\w\.\-\!\#\^\~]{1,40}\$?)\s+\w+='] |
| removed_attribute | DupFields |  | N/A |