# Code Changes for cloudflare-insights-http-response-success (Event Builder)

| Code Change | Field Name | 2025.11.1 | 2025.12.1 |
|-------------|------------|-----------|------------|
| edit_conditions | expression | InList(type, 'cloudflare-insights-json-http-response-edgeresponsestatus') && exists(http_response_code) && StartsWithAny(http_response_code,'1','2','3') | InList(type, 'cloudflare-insights-json-http-response-edgeresponsestatus') && StartsWithAny(http_response_code,'1','2','3') |