# Code Changes for digital-network-http-session-success (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression | InList(type, 'digitalarts-ifb-str-http-session-proxyifilter') && exists(http_response_code) && StartsWithAny(http_response_code,'1','2','3') | InList(type, 'digitalarts-ifb-str-http-session-proxyifilter') && StartsWithAny(http_response_code,'1','2','3') |