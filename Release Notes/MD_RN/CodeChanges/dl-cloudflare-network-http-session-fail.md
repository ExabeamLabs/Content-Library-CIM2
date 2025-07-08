# Code Changes for dl-cloudflare-network-http-session-fail (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression | InList(type, 'cloudflare-waf-json-http-session-firewall') && exists(http_response_code) && !StartsWithAny(http_response_code,'1','2','3') | InList(type, 'cloudflare-waf-json-http-session-firewall') && !StartsWithAny(http_response_code,'1','2','3') |