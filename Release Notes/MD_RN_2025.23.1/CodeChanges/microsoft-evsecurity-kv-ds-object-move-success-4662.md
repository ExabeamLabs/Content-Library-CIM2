# Code Changes for microsoft-evsecurity-kv-ds-object-move-success-4662 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'attributes', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'object', 'object_name', 'object_server', 'object_type', 'operation_type', 'time', 'user', 'user_sid'] |
| edit_regex_field | object_name |  | ['Object Name:\s*({object}({object_name}\S.*?))\s*Handle ID:'] |
| added_regex_field | object |  | ['Object Name:\s*({object}({object_name}\S.*?))\s*Handle ID:'] |
| removed_attribute | DupFields |  | N/A |