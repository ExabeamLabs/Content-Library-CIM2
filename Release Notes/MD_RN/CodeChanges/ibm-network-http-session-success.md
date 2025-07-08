# Code Changes for ibm-network-http-session-success (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression | InList(type, 'ibm-sam-str-http-session-webseald') && exists(http_response_code) && StartsWithAny(http_response_code,'1','2','3') | InList(type, 'ibm-sam-str-http-session-webseald') && StartsWithAny(http_response_code,'1','2','3') |