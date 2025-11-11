# Code Changes for cisco-fp-kv-network-traffic-estreamer (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'bytes_in', 'bytes_out', 'category', 'connection_type', 'dest_ip', 'dest_port', 'egress_zone', 'host', 'ingress_zone', 'initiator_packets', 'nap_policy', 'policy_name', 'protocol', 'reputation', 'responder_packets', 'response_type', 'result', 'rule', 'src_ip', 'src_port', 'tcp_flags', 'user'] |
| edit_regex_field | result |  | ['\WAccessControlRuleAction:\s*({action}({result}[^,]+))', 'exa_json_path=$.message,exa_regex=\WAccessControlRuleAction:\s*({action}({result}[^,]+))'] |
| added_regex_field | action |  | ['\WAccessControlRuleAction:\s*({action}({result}[^,]+))', 'exa_json_path=$.message,exa_regex=\WAccessControlRuleAction:\s*({action}({result}[^,]+))'] |
| removed_attribute | DupFields |  | N/A |