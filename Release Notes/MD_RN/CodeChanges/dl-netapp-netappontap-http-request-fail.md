# Code Changes for dl-netapp-netappontap-http-request-fail (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression | InList(type, 'netapp-netappontap-str-http-request-netapp') && exists(http_response_code) && !startsWithAny(http_response_code, '1','2','3') && !InList(toLower(result), 'pending') | InList(type, 'netapp-netappontap-str-http-request-netapp') && !startsWithAny(http_response_code, '1','2','3') && !InList(toLower(result), 'pending') |