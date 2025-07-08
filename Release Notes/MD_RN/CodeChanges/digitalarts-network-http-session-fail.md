# Code Changes for digitalarts-network-http-session-fail (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression | InList(type, 'digitalarts-ifb-csv-http-session-proxy') && exists(http_response_code) && !StartsWithAny(http_response_code,'1','2','3') | InList(type, 'digitalarts-ifb-csv-http-session-proxy') && !StartsWithAny(http_response_code,'1','2','3') |