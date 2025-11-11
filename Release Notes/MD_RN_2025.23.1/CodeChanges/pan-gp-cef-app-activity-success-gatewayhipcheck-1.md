# Code Changes for pan-gp-cef-app-activity-success-gatewayhipcheck-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'app', 'domain', 'event_name', 'host', 'operation', 'os', 'result', 'src_host', 'src_ip', 'src_port', 'src_translated_ip', 'time', 'user'] |
| edit_regex_field | event_name |  | ['({operation}({event_name}gateway-hip-check))'] |
| added_regex_field | operation |  | ['({operation}({event_name}gateway-hip-check))'] |
| removed_attribute | DupFields |  | N/A |