# Code Changes for checkpoint-tp-kv-alert-trigger-success-actiondetect (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'action', 'additional_info', 'alert_name', 'alert_severity', 'alert_source', 'alert_subject', 'alert_type', 'attack', 'attack_info', 'confidence_level', 'dest_ip', 'dest_port', 'domain', 'first_name', 'host', 'http_response_code', 'last_name', 'malware_action', 'method', 'origin_ip', 'origin_name', 'product_name', 'protection_name', 'protocol', 'rule', 'rule_id', 'smartdefense_profile', 'src_host', 'src_ip', 'src_port', 'time', 'user', 'user_ou', 'web_domain'] |
| added_regex_field | alert_source |  | ['\Wproduct:"({alert_source}[^"]+)'] |
| added_regex_field | alert_subject |  | ['\Wattack:"({alert_subject}[^"]+)'] |
| removed_attribute | DupFields |  | N/A |