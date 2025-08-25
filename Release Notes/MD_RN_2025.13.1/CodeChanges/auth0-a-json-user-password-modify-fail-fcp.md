# Code Changes for auth0-a-json-user-password-modify-fail-fcp (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | operation_type |  | ['"type":"({operation_type}[^",]+)"', 'exa_json_path=$.message.type,exa_regex=({operation_type}[^",]+)', 'exa_regex=({operation_type}fcp)'] |