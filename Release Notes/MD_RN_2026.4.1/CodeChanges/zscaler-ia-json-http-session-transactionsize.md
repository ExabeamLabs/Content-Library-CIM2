# Code Changes for zscaler-ia-json-http-session-transactionsize (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | http_response_code |  | ['"status":"({http_response_code}\d{1,3})"', 'exa_regex="status":"({http_response_code}\d{1,3})"'] |