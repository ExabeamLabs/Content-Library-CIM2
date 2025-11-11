# Code Changes for microsoft-evsecurity-csv-ds-object-activity-success-4662 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['attribute', 'dest_domain', 'dest_user', 'dest_user_sid', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'object', 'object_name', 'object_type', 'operation', 'properties', 'result', 'time', 'user', 'user_sid'] |
| edit_regex_field | object_name |  | ['"(An operation was performed on an object)",("[^"]+",){3}"({object}({object_name}[^"]+))'] |
| added_regex_field | object |  | ['"(An operation was performed on an object)",("[^"]+",){3}"({object}({object_name}[^"]+))'] |
| removed_attribute | DupFields |  | N/A |