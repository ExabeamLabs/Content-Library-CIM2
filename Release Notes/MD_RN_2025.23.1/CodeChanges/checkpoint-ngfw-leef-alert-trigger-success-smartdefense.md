# Code Changes for checkpoint-ngfw-leef-alert-trigger-success-smartdefense (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_name', 'alert_severity', 'alert_source', 'alert_subject', 'alert_type', 'attack_info', 'confidence_level', 'dest_host', 'dest_ip', 'dest_port', 'domain', 'event_name', 'full_name', 'host', 'log_uid', 'origin_sic_name', 'performance_impact', 'product_name', 'protection_id', 'protection_name', 'protection_type', 'protocol', 'rule', 'rule_count', 'rule_id', 'smartdefense_profile', 'src_host', 'src_ip', 'src_port', 'time', 'url', 'user'] |
| added_regex_field | alert_subject |  | ['\Wattack_info=({alert_subject}.+?)(\s+\w+:?=|\s*$)'] |
| added_regex_field | protection_name |  | ['\Wsignature=({protection_name}.+?)(\s+\w+:?=|\s*$)'] |
| removed_attribute | DupFields |  | N/A |