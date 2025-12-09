# Code Changes for crowdstrike-falcon-json-app-notification-success-streamstopped (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['aid', 'app', 'email_address', 'email_domain', 'event_category', 'event_name', 'operation', 'result', 'time', 'user'] |
| edit_regex_field | event_name |  | ['"OperationName":"({operation}({event_name}[^"]+))'] |
| added_regex_field | operation |  | ['"OperationName":"({operation}({event_name}[^"]+))'] |
| removed_attribute | DupFields |  | N/A |