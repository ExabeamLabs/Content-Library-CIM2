# Code Changes for juniper-ps-kv-vpn-logout-success-firewall-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'domain', 'email_address', 'email_domain', 'event_code', 'host', 'realm', 'role', 'src_ip', 'time', 'user'] |
| added_regex_field | dest_host |  | ['vpn=({dest_host}[^\s]+)'] |
| removed_attribute | DupFields |  | N/A |