# Code Changes for venofi-tlp-json-app-activity-success-tls (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'device_ip', 'event_code', 'event_name', 'host', 'object', 'object_id', 'object_name', 'severity', 'time', 'user'] |
| edit_regex_field | additional_info |  | ['"description":"({event_name}({additional_info}[^"]+))'] |
| added_regex_field | event_name |  | ['"description":"({event_name}({additional_info}[^"]+))'] |
| removed_attribute | DupFields |  | N/A |