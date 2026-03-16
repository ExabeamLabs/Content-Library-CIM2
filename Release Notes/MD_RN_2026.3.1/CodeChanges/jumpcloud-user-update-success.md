# Code Changes for jumpcloud-user-update-success (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression |  | InList(type, 'jumpcloud-jc-json-directoryinsights-events') &&  InList(toLower(event_category), 'user_update', 'user_update_provision','admin_update')  && (InList(toLower(result),'true') || !exists(result))  |