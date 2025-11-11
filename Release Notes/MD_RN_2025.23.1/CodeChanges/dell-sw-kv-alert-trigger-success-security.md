# Code Changes for dell-sw-kv-alert-trigger-success-security (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'additional_info', 'alert_name', 'alert_severity', 'alert_subject', 'alert_type', 'category_id', 'dest_interface', 'dest_ip', 'dest_mac', 'dest_port', 'email_address', 'event_name', 'firewall', 'message_id', 'packets_in', 'packets_out', 'protocol', 'rule', 'severity', 'src_interface', 'src_ip', 'src_mac', 'src_port', 'time', 'user'] |
| edit_regex_field | message_id |  | ['\sm=({alert_type}({message_id}\d+))'] |
| added_regex_field | alert_type |  | ['\sm=({alert_type}({message_id}\d+))'] |
| removed_attribute | DupFields |  | N/A |