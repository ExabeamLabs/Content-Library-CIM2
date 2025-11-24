# Code Changes for tenable-tvm-json-alert-trigger-success-plugintext (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'additional_info', 'alert_name', 'alert_severity', 'alert_subject', 'cve_id', 'cvss_base_score', 'domain', 'host', 'original_risk_score', 'os', 'protocol', 'see_also', 'solution', 'src_host', 'src_ip', 'time'] |
| edit_regex_field | alert_name |  | ['"name":\s*"({alert_subject}({alert_name}[^"]+))', '"synopsis":\s*"({alert_subject}({alert_name}[^"]+?))"'] |
| added_regex_field | alert_subject |  | ['"name":\s*"({alert_subject}({alert_name}[^"]+))', '"synopsis":\s*"({alert_subject}({alert_name}[^"]+?))"'] |
| removed_attribute | DupFields |  | N/A |