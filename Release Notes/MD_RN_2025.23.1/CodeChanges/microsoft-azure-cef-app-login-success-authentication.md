# Code Changes for microsoft-azure-cef-app-login-success-authentication (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | event_name |  | ['operationName\":\"({operation}({event_name}[^\"]+))\"'] |
| edit_regex_field | operation |  | ['([^\|]*\|){5}({operation}[^\|]+)', '\Wact=({operation}[^=]+)\s+(\w+=|$)', '\WflexString1=({operation}[^=]+)\s+(\w+=|$)', 'operationName\":\"({operation}({event_name}[^\"]+))\"'] |
| removed_attribute | DupFields |  | N/A |