# Code Changes for juniper-ps-kv-vpn-login-success-connectionwith (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'additional_info', 'bytes_in', 'bytes_out', 'dest_host', 'dest_ip', 'dest_port', 'firewall', 'host', 'op', 'protocol', 'realm', 'result', 'role', 'session_duration', 'src_ip', 'src_port', 'time', 'user', 'vpn_client', 'vpn_client_type'] |
| added_regex_field | account |  | ['\Wuser=([^\\]+\\)?({account}[\w\.\-\!\#\^\~]{1,40}\$?)'] |
| removed_attribute | DupFields |  | N/A |