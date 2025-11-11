# Code Changes for checkpoint-tm-kv-app-activity-success-threatemulation (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'action', 'additional_info', 'alert_name', 'alert_severity', 'app_protocol', 'bytes', 'bytes_in', 'bytes_out', 'confidence_level', 'dest_host', 'dest_ip', 'dest_port', 'dest_translated_ip', 'dest_translated_port', 'domain', 'email_address', 'email_domain', 'event_name', 'failure_reason', 'first_name', 'host', 'interface_name', 'last_name', 'malware_action', 'malware_family', 'malware_id', 'malware_name', 'origin_ip', 'origin_name', 'policy_name', 'product_name', 'protection_name', 'protection_type', 'protocol', 'resource', 'result', 'rule', 'rule_id', 'smartdefense_profile', 'src_host', 'src_ip', 'src_port', 'src_translated_ip', 'src_translated_port', 'time', 'url', 'user', 'user_agent', 'vendor_name'] |
| edit_regex_field | action |  | ['\Waction:\"+({result}({action}[^\"]+))', 'action_details:"({result}({action}[^"]+))'] |
| added_regex_field | bytes |  | ['\Wsent_bytes:\"+({bytes}\d+)'] |
| added_regex_field | result |  | ['\Waction:\"+({result}({action}[^\"]+))', 'action_details:"({result}({action}[^"]+))'] |
| removed_attribute | DupFields |  | N/A |