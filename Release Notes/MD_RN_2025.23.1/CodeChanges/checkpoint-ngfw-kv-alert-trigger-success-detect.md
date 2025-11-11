# Code Changes for checkpoint-ngfw-kv-alert-trigger-success-detect (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_name', 'alert_severity', 'alert_type', 'confidence_level', 'dest_ip', 'dest_port', 'host', 'origin_ip', 'origin_name', 'product_name', 'protection_name', 'protocol', 'result', 'rule', 'rule_id', 'smartdefense_profile', 'src_ip', 'src_port', 'time', 'user_ou'] |
| added_regex_field | alert_name |  | ['\Wprotection_name:({alert_name}[^"]+)'] |
| removed_attribute | DupFields |  | N/A |