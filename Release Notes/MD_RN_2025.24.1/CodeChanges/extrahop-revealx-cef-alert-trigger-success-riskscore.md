# Code Changes for extrahop-revealx-cef-alert-trigger-success-riskscore (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_id', 'alert_name', 'alert_severity', 'alert_type', 'bytes_in', 'bytes_out', 'dest_host', 'dest_ip', 'dest_mac', 'dest_port', 'event_name', 'host', 'original_risk_score', 'src_host', 'src_ip', 'src_mac', 'src_port', 'time', 'user'] |
| edit_regex_field | original_risk_score |  | ['cn1=({alert_severity}({original_risk_score}\d+))\s+cn1Label=riskScore', 'cn2=({alert_severity}({original_risk_score}\d+))\s+cn2Label=riskScore'] |
| added_regex_field | alert_severity |  | ['cn1=({alert_severity}({original_risk_score}\d+))\s+cn1Label=riskScore', 'cn2=({alert_severity}({original_risk_score}\d+))\s+cn2Label=riskScore'] |
| removed_attribute | DupFields |  | N/A |