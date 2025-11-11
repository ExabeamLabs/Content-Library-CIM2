# Code Changes for juniper-ps-kv-vpn-login-success-firewall-3 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'dest_host', 'domain', 'email_address', 'email_domain', 'event_code', 'host', 'realm', 'role', 'src_ip', 'src_port', 'time', 'user'] |
| added_regex_field | dest_host |  | ['vpn=({dest_host}[^\s]+)'] |
| removed_attribute | DupFields |  | N/A |