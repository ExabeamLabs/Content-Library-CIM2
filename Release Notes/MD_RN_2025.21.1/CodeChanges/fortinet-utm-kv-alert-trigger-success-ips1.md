# Code Changes for fortinet-utm-kv-alert-trigger-success-ips1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'additional_info', 'alert_name', 'alert_severity', 'alert_subject', 'alert_type', 'dest_ip', 'dest_port', 'host', 'more_info', 'protocol', 'src_ip', 'src_port', 'time', 'tz', 'user', 'web_domain'] |
| edit_regex_field | alert_name |  | ['\Wattack="({alert_subject}({alert_name}[^"]+))"'] |
| added_regex_field | alert_subject |  | ['\Wattack="({alert_subject}({alert_name}[^"]+))"'] |
| removed_attribute | DupFields |  | N/A |