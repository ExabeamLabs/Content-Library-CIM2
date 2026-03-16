# Code Changes for dell-network-http-session-success (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression |  | InList(type, 'dell-sw-kv-http-session-category') && (!exists(action) || toLower(action)!= 'drop') |