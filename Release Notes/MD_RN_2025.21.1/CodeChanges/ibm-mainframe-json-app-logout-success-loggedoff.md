# Code Changes for ibm-mainframe-json-app-logout-success-loggedoff (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'event_code', 'event_name', 'operation', 'severity', 'time', 'user'] |
| edit_regex_field | event_name |  | ['({operation}({event_name}LOGGED OFF))'] |
| added_regex_field | operation |  | ['({operation}({event_name}LOGGED OFF))'] |
| removed_attribute | DupFields |  | N/A |