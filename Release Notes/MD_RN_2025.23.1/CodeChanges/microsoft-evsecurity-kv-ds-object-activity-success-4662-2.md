# Code Changes for microsoft-evsecurity-kv-ds-object-activity-success-4662-2 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'access_mask', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'object', 'object_name', 'object_server', 'object_type', 'operation', 'operation_type', 'properties', 'time', 'user', 'user_sid', 'user_upn'] |
| edit_regex_field | object_name |  | ['Object Name:(\\t|\\r|\\n)*\s*(|({object}({object_name}[^:]+?)))(\\t|\\r|\\n)*\s*Handle ID:'] |
| added_regex_field | object |  | ['Object Name:(\\t|\\r|\\n)*\s*(|({object}({object_name}[^:]+?)))(\\t|\\r|\\n)*\s*Handle ID:'] |
| removed_attribute | DupFields |  | N/A |