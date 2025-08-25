# Code Changes for f5-dc-http-session-success (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression |  | InList(type, 'f5-dc-json-http-session-success-fail-wafaction') && startsWithAny(http_response_code, '1','2','3') |