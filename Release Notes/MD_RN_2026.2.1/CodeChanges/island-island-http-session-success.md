# Code Changes for island-island-http-session-success (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression |  | InList(type, 'island-islandbrowser-json-http-session-island', 'island-islandbrowser-json-http-session-message') && (!exists(result) || InList(toLower(result), 'allowed')) |