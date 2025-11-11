# Code Changes for ivanti-ps-kv-vpn-authentication-fail-eam24460 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'dest_host', 'dest_ip', 'domain', 'email_address', 'email_domain', 'event_code', 'event_name', 'failure_reason', 'firewall', 'host', 'protocol', 'realm', 'role', 'session_id', 'src_ip', 'time', 'user', 'user_agent', 'vpn_client', 'vpn_client_type'] |
| edit_regex_field | event_name |  | ['({failure_reason}({event_name}NeedHostChecker))', '\smsg="({event_name}[^"]+)"'] |
| added_regex_field | failure_reason |  | ['({failure_reason}({event_name}NeedHostChecker))'] |
| removed_attribute | DupFields |  | N/A |