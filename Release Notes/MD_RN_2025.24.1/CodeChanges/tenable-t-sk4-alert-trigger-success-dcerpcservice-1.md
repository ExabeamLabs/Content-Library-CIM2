# Code Changes for tenable-t-sk4-alert-trigger-success-dcerpcservice-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_name', 'alert_severity', 'alert_status', 'alert_subject', 'alert_type', 'cve_id', 'cvss_base_score', 'exploit_code_maturity', 'host', 'original_risk_score', 'protocol', 'see_also', 'solution', 'src_ip', 'src_port', 'time'] |
| edit_regex_field | alert_name |  | ['"name"+:\s*"+({alert_type}({alert_name}[^"]+))'] |
| added_regex_field | alert_type |  | ['"name"+:\s*"+({alert_type}({alert_name}[^"]+))'] |
| removed_attribute | DupFields |  | N/A |