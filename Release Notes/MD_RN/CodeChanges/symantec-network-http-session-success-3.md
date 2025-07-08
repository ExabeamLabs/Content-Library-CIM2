# Code Changes for symantec-network-http-session-success-3 (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression | InList(type,'symantec-wss-sk4-http-session-denied') && exists(http_response_code) && StartsWithAny(http_response_code,'1','2','3') | InList(type,'symantec-wss-sk4-http-session-denied') && StartsWithAny(http_response_code,'1','2','3') |