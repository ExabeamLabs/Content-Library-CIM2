# Code Changes for sap-sf-mix-app-activity-processmulee (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'app', 'category', 'correlation_id', 'event_name', 'host', 'object_id', 'object_type', 'operation', 'result', 'severity', 'src_ip', 'src_port', 'time'] |
| edit_regex_field | event_name |  | ['action=({operation}({event_name}[^,]+))'] |
| added_regex_field | operation |  | ['action=({operation}({event_name}[^,]+))'] |
| removed_attribute | DupFields |  | N/A |