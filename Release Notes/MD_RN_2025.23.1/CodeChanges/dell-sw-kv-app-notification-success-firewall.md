# Code Changes for dell-sw-kv-app-notification-success-firewall (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_name', 'alert_severity', 'alert_type', 'bytes_in', 'bytes_out', 'category_id', 'event_name', 'firewall', 'interface', 'message_id', 'time'] |
| edit_regex_field | message_id |  | ['\sm=({alert_type}({message_id}\d+))', '\sm=({message_id}\d+)'] |
| added_regex_field | alert_type |  | ['\sm=({alert_type}({message_id}\d+))'] |
| removed_attribute | DupFields |  | N/A |