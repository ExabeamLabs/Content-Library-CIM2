# Code Changes for blackberry-protect-xml-alert-trigger-success-32 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['alert_name', 'alert_type', 'host', 'malware_url', 'src_host', 'src_ip', 'src_mac', 'src_port', 'time'] |
| edit_regex_field | alert_type |  | ['({alert_name}({alert_type}A potentially malicious Active script was Detected))'] |
| added_regex_field | alert_name |  | ['({alert_name}({alert_type}A potentially malicious Active script was Detected))'] |
| removed_attribute | DupFields |  | N/A |