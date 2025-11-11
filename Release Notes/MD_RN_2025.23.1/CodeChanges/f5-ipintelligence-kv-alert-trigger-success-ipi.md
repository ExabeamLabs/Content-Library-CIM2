# Code Changes for f5-ipintelligence-kv-alert-trigger-success-ipi (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['alert_name', 'alert_severity', 'alert_type', 'protocol', 'src_ip', 'src_port', 'time'] |
| edit_regex_field | alert_name |  | ['ip_intelligence_policy_name\s*=\s*(|({alert_type}({alert_name}[^,]+))),', 'ip_intelligence_threat_name\s*=\s*(|({alert_type}({alert_name}[^,]+))),'] |
| added_regex_field | alert_type |  | ['ip_intelligence_policy_name\s*=\s*(|({alert_type}({alert_name}[^,]+))),', 'ip_intelligence_threat_name\s*=\s*(|({alert_type}({alert_name}[^,]+))),'] |
| removed_attribute | DupFields |  | N/A |