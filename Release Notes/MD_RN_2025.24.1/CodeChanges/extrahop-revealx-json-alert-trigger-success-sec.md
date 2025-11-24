# Code Changes for extrahop-revealx-json-alert-trigger-success-sec (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_name', 'alert_severity', 'alert_type', 'dest_host', 'dest_ip', 'dest_port', 'dns_query', 'domain', 'host', 'original_risk_score', 'src_host', 'src_ip', 'src_port', 'status_msg', 'sub_domain', 'time'] |
| edit_regex_field | alert_name |  | ['"title":"({alert_type}({alert_name}[^"]+))'] |
| edit_regex_field | original_risk_score |  | ['"riskScore":(null|({alert_severity}({original_risk_score}\d+)))'] |
| added_regex_field | alert_severity |  | ['"riskScore":(null|({alert_severity}({original_risk_score}\d+)))'] |
| added_regex_field | alert_type |  | ['"title":"({alert_type}({alert_name}[^"]+))'] |
| removed_attribute | DupFields |  | N/A |