# Code Changes for netskope-network-network-traffic-success-1 (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression | InList(type, 'netskope-webtx-json-network-traffic-ipsecnetworksecurity') && NOT exists(http_response_code) | InList(type, 'netskope-webtx-json-network-traffic-ipsecnetworksecurity') &&  !exists(http_response_code) |