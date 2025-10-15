# Code Changes for sentinelone-network-http-session-success-1 (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression |  | (InList(type, 'sentinelone-singularityp-json-alert-trigger-success-url-1') && toLower(event_name)='http') && InList(toLower(alert_name), 'get','post','head','put','delete','options','patch') |