# Code Changes for infoblox-bddi-cef-network-traffic-threat (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'alert_name', 'alert_severity', 'alert_type', 'dest_ip', 'dest_port', 'dns_query', 'host', 'rule_id', 'src_ip', 'src_port'] |
| edit_regex_field | dns_query |  | ['fqdn=(NA|({dns_query}[\w\-.]+))'] |
| removed_regex_field | operation |  | [] |
| added_regex_field | alert_type |  | ['cat="({alert_type}[^"]+)'] |