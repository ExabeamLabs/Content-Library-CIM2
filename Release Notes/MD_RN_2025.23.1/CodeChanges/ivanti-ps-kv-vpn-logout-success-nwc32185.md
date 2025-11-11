# Code Changes for ivanti-ps-kv-vpn-logout-success-nwc32185 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'dest_host', 'dest_ip', 'domain', 'email_address', 'email_domain', 'event_code', 'event_name', 'failure_reason', 'firewall', 'host', 'protocol', 'realm', 'role', 'session_id', 'src_ip', 'time', 'user', 'user_agent', 'vpn_client', 'vpn_client_type'] |
| added_regex_field | failure_reason |  | ['\smsg="({failure_reason}.+?)$'] |
| removed_attribute | DupFields |  | N/A |