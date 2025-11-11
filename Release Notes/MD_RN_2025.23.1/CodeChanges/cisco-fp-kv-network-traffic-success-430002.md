# Code Changes for cisco-fp-kv-network-traffic-success-430002 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'bytes_in', 'bytes_out', 'dest_interface', 'dest_ip', 'dest_port', 'device_id', 'egress_zone', 'host', 'ingress_zone', 'packets_in', 'packets_out', 'policy_name', 'protocol', 'result', 'src_interface', 'src_ip', 'src_port', 'time'] |
| added_regex_field | action |  | ['AccessControlRuleAction:\s*({action}[^,]+)'] |
| removed_attribute | DupFields |  | N/A |