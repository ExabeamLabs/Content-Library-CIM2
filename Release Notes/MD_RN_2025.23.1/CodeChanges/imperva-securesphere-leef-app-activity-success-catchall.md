# Code Changes for imperva-securesphere-leef-app-activity-success-catchall (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_severity', 'domain', 'event_name', 'operation', 'time', 'user'] |
| edit_regex_field | operation |  | ['SecureSphere\|[^|]+?\|({event_name}({operation}[^\|]+))\|'] |
| added_regex_field | event_name |  | ['SecureSphere\|[^|]+?\|({event_name}({operation}[^\|]+))\|'] |
| removed_attribute | DupFields |  | N/A |