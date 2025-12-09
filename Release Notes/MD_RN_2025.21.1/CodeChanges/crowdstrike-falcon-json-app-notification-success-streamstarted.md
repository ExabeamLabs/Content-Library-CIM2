# Code Changes for crowdstrike-falcon-json-app-notification-success-streamstarted (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['cid', 'event_category', 'event_name', 'operation', 'result', 'service_name', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | event_name |  | ['"OperationName":"({operation}({event_name}[^"]+))'] |
| added_regex_field | operation |  | ['"OperationName":"({operation}({event_name}[^"]+))'] |
| removed_attribute | DupFields |  | N/A |