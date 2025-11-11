# Code Changes for citrix-cgateway-str-app-login-success-sslvpnlogin (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['app', 'dest_ip', 'dest_port', 'domain', 'email_address', 'email_domain', 'host', 'src_ip', 'src_port', 'src_translated_ip', 'time', 'user', 'user_agent', 'vpn_client_type'] |
| edit_regex_field | vpn_client_type |  | ['SSLVPN_client_type\s*({app}({vpn_client_type}[^\s]+)) - Group'] |
| added_regex_field | app |  | ['SSLVPN_client_type\s*({app}({vpn_client_type}[^\s]+)) - Group'] |
| removed_attribute | DupFields |  | N/A |