# Code Changes for kasada-network-http-session-fail (Event Builder)

| Code Change | Field Name | 2025.11.1 | 2025.12.1 |
|-------------|------------|-----------|------------|
| edit_conditions | expression | InList(type,'kasada-k-json-http-session-nonstatic') && ((exists(http_response_code) && !StartsWithAny(http_response_code,'1','2','3'))) | InList(type,'kasada-k-json-http-session-nonstatic') && !StartsWithAny(http_response_code,'1','2','3') |