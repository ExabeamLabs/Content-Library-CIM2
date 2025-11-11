# Code Changes for dell-sw-mix-app-activity-assignedipaddress (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_name', 'alert_severity', 'alert_type', 'category_id', 'dest_ip', 'dest_mac', 'dest_port', 'event_name', 'firewall', 'host', 'message_id', 'time'] |
| edit_regex_field | message_id |  | ['\sm=({alert_type}({message_id}\d+))'] |
| added_regex_field | alert_type |  | ['\sm=({alert_type}({message_id}\d+))'] |
| removed_attribute | DupFields |  | N/A |