# Code Changes for microsoft-o365-json-alert-trigger-success-securitythreatdetected-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['alert_id', 'alert_name', 'alert_severity', 'alert_type', 'email_address', 'email_domain', 'event_name', 'full_name', 'result', 'src_ip', 'src_port', 'time'] |
| edit_regex_field | alert_name |  | ['"riskEventTypes":\["({alert_type}({alert_name}[^"]+))"', '"riskType":"({alert_type}({alert_name}[^"]+))'] |
| added_regex_field | alert_type |  | ['"riskEventTypes":\["({alert_type}({alert_name}[^"]+))"', '"riskType":"({alert_type}({alert_name}[^"]+))'] |
| removed_attribute | DupFields |  | N/A |