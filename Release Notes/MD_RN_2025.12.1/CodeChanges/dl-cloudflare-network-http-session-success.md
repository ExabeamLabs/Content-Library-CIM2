# Code Changes for dl-cloudflare-network-http-session-success (Event Builder)

| Code Change | Field Name | 2025.11.1 | 2025.12.1 |
|-------------|------------|-----------|------------|
| edit_conditions | expression | InList(type, 'cloudflare-waf-json-http-session-firewall') && exists(http_response_code) && StartsWithAny(http_response_code,'1','2','3') | InList(type, 'cloudflare-waf-json-http-session-firewall') && StartsWithAny(http_response_code,'1','2','3') |