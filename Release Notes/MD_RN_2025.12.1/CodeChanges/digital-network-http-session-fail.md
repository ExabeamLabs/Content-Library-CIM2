# Code Changes for digital-network-http-session-fail (Event Builder)

| Code Change | Field Name | 2025.11.1 | 2025.12.1 |
|-------------|------------|-----------|------------|
| edit_conditions | expression | InList(type,'digitalarts-ifb-str-http-session-proxyifilter') && exists(http_response_code) && !StartsWithAny(http_response_code,'1','2','3') | InList(type,'digitalarts-ifb-str-http-session-proxyifilter') && !StartsWithAny(http_response_code,'1','2','3') |