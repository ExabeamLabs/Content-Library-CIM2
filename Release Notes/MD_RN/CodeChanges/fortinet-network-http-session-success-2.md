# Code Changes for fortinet-network-http-session-success-2 (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression | InList(type, 'fortinet-fortiweb-kv-http-session-traffic','fortinet-fortiweb-kv-http-session-traffic-http') && exists(http_response_code) && StartsWithAny(http_response_code,'1','2','3') | InList(type, 'fortinet-fortiweb-kv-http-session-traffic','fortinet-fortiweb-kv-http-session-traffic-http') && StartsWithAny(http_response_code,'1','2','3') |