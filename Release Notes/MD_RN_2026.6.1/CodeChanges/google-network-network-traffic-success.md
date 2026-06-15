# Code Changes for google-network-network-traffic-success (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression |  | InList(type, 'google-cloudplatform-json-network-traffic-success-payload', 'google-cloudplatform-sk4-network-traffic-success-payload') && (InList(toLower(action), 'allowed') or !exists(action)) |