# Code Changes for f5-silverline-kv-alert-trigger-ipi (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['alert_name', 'alert_severity', 'host', 'operation', 'policy_name', 'protocol', 'rule', 'rule_type', 'src_ip', 'src_port', 'time'] |
| edit_regex_field | policy_name |  | ['ip_intelligence_policy_name="({alert_name}({policy_name}[^"]+))"'] |
| added_regex_field | alert_name |  | ['ip_intelligence_policy_name="({alert_name}({policy_name}[^"]+))"'] |
| removed_attribute | DupFields |  | N/A |