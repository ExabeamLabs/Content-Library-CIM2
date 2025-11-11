# Code Changes for checkpoint-network-alert (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'action', 'alert_name', 'alert_severity', 'alert_subject', 'alert_type', 'attack', 'attack_info', 'confidence_level', 'dest_ip', 'dest_port', 'domain', 'first_name', 'host', 'last_name', 'origin_ip', 'origin_name', 'product_name', 'protection_name', 'protocol', 'rule', 'rule_id', 'smartdefense_profile', 'src_host', 'src_ip', 'src_port', 'time', 'user', 'user_ou'] |
| added_regex_field | alert_subject |  | ['\Wattack:"({alert_subject}[^"]+)'] |
| removed_attribute | DupFields |  | N/A |