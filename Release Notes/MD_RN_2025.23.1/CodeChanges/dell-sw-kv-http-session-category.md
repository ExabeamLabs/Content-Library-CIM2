# Code Changes for dell-sw-kv-http-session-category (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'additional_info', 'alert_name', 'alert_severity', 'alert_type', 'bytes_in', 'bytes_out', 'category', 'category_id', 'dest_interface', 'dest_ip', 'dest_mac', 'dest_port', 'email_address', 'firewall', 'message_id', 'protocol', 'rule', 'src_interface', 'src_ip', 'src_mac', 'src_port', 'time', 'user', 'web_domain'] |
| edit_regex_field | message_id |  | ['\sm=({alert_type}({message_id}\d+))'] |
| added_regex_field | alert_type |  | ['\sm=({alert_type}({message_id}\d+))'] |
| removed_attribute | DupFields |  | N/A |