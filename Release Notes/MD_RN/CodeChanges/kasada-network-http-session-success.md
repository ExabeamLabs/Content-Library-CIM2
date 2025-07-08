# Code Changes for kasada-network-http-session-success (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression | InList(type, 'kasada-k-json-http-session-nonstatic') && exists(http_response_code) && StartsWithAny(http_response_code,'1','2','3') | InList(type, 'kasada-k-json-http-session-nonstatic') && StartsWithAny(http_response_code,'1','2','3') |