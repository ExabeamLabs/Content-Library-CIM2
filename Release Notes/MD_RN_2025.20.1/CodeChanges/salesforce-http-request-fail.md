# Code Changes for salesforce-http-request-fail (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression |  | InList(type,'salesforce-sf-json-app-activity-success-loginhistory')  && InList(toLower(event_category), 'restapi') && !StartsWithAny(http_response_code,'1','2','3') |