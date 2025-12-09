# Code Changes for cisco-duo-json-app-activity-success-api (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['app', 'device_name', 'email_address', 'object', 'operation', 'time', 'user'] |
| edit_regex_field | object |  | ['"type":\s*"({device_name}({object}[^"]+))"'] |
| added_regex_field | device_name |  | ['"type":\s*"({device_name}({object}[^"]+))"'] |
| removed_attribute | DupFields |  | N/A |