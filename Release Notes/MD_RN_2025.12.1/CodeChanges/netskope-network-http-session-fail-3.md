# Code Changes for netskope-network-http-session-fail-3 (Event Builder)

| Code Change | Field Name | 2025.11.1 | 2025.12.1 |
|-------------|------------|-----------|------------|
| edit_conditions | expression | InList(type, 'netskope-webtx-json-network-traffic-ipsecnetworksecurity') and exists(http_response_code) and !startsWithAny(http_response_code, '1', '2', '3') | InList(type, 'netskope-webtx-json-network-traffic-ipsecnetworksecurity') and startsWithAny(http_response_code, '4', '5', '6') |