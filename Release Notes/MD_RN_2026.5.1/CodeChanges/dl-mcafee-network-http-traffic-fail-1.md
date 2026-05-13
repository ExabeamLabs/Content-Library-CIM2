# Code Changes for dl-mcafee-network-http-traffic-fail-1 (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression |  | InList(type, 'mcafee-wg-cef-http-session-gateway') && (exists(mime) && StartsWithAny(toLower(mime),'image','text/css','application','audio','text','video')) && !StartsWithAny(http_response_code,'1','2','3') && not (exists(category) && containsAny(toLower(category),'web ads')) |