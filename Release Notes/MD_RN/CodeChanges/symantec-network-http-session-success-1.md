# Code Changes for symantec-network-http-session-success-1 (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression | InList(type, 'symantec-fireglass-cef-http-session-url','symantec-wss-cef-http-session-request','symantec-wss-sk4-http-session-symantecwss','symantec-wss-sk4-http-session-proxied','symantec-wss-sk4-http-session-observed') and exists(http_response_code) and StartsWithAny(http_response_code,'1','2','3') | InList(type, 'symantec-fireglass-cef-http-session-url','symantec-wss-cef-http-session-request','symantec-wss-sk4-http-session-symantecwss','symantec-wss-sk4-http-session-proxied','symantec-wss-sk4-http-session-observed') and StartsWithAny(http_response_code,'1','2','3') |