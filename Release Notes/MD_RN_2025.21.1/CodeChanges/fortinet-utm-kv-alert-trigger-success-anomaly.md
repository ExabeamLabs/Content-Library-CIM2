# Code Changes for fortinet-utm-kv-alert-trigger-success-anomaly (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'additional_info', 'alert_id', 'alert_name', 'alert_severity', 'alert_subject', 'alert_type', 'dest_ip', 'dest_port', 'host', 'malware_url', 'protocol', 'src_ip', 'src_port', 'time', 'tz', 'user'] |
| edit_regex_field | alert_name |  | ['\Wattack="({alert_subject}({alert_name}[^"]+))"'] |
| added_regex_field | alert_subject |  | ['\Wattack="({alert_subject}({alert_name}[^"]+))"'] |
| removed_attribute | DupFields |  | N/A |