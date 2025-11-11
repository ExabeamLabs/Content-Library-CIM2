# Code Changes for microsoft-evsecurity-kv-ds-object-activity-success-4662-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'action', 'attribute', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'object', 'object_name', 'object_server', 'object_type', 'properties', 'time', 'user'] |
| edit_regex_field | object_name |  | ['Object Name:\s*({object}({object_name}.+?))\s*Handle ID:'] |
| added_regex_field | object |  | ['Object Name:\s*({object}({object_name}.+?))\s*Handle ID:'] |
| removed_attribute | DupFields |  | N/A |