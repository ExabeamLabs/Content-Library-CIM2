# Code Changes for crowdstrike-falcon-json-configuration-modify-success-firewall (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_name', 'action', 'additional_info', 'aid', 'aip', 'cid', 'email_address', 'email_domain', 'event_code', 'host', 'operation', 'os', 'rule', 'rule_id', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | operation |  | ['\"event_simpleName\":\"({event_code}({operation}[^\"]+))'] |
| added_regex_field | event_code |  | ['\"event_simpleName\":\"({event_code}({operation}[^\"]+))'] |
| removed_attribute | DupFields |  | N/A |