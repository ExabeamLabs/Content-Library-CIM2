# Code Changes for sophos-xgfirewall-kv-network-traffic-success-firewallrule (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'dest_country', 'dest_country_code', 'dest_interface', 'dest_ip', 'dest_mac', 'dest_network_zone', 'dest_port', 'dest_translated_ip', 'dest_translated_port', 'device_id', 'duration', 'email_address', 'email_domain', 'event_category', 'event_id', 'host', 'policy_name', 'priority', 'protocol', 'result', 'rule_id', 'src_country', 'src_country_code', 'src_interface', 'src_ip', 'src_mac', 'src_network_zone', 'src_port', 'src_translated_ip', 'src_translated_port', 'subtype', 'time', 'user'] |
| edit_regex_field | subtype |  | ['\slog_subtype="({action}({subtype}\S+))?"\s', '\slog_subtype="({result}({subtype}\S+))?"\s'] |
| added_regex_field | result |  | ['\slog_subtype="({result}({subtype}\S+))?"\s', '\sstatus="({result}\S+)?"\s'] |
| removed_attribute | DupFields |  | N/A |