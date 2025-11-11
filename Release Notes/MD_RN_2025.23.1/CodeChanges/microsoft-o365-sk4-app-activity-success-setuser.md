# Code Changes for microsoft-o365-sk4-app-activity-success-setuser (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['app', 'email_address', 'event_name', 'host', 'object', 'operation', 'result', 'src_ip', 'src_port', 'time', 'user_agent'] |
| edit_regex_field | operation |  | ['\"Operation\":\"({event_name}({operation}[^\"]+))'] |
| added_regex_field | event_name |  | ['\"Operation\":\"({event_name}({operation}[^\"]+))'] |
| removed_attribute | DupFields |  | N/A |