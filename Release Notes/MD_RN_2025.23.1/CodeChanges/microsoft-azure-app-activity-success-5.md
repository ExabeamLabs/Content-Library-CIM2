# Code Changes for microsoft-azure-app-activity-success-5 (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression |  | InList(type, 'azure-azuread-json-app-activity-useractivitydisplayname', 'azure-azuread-json-app-activity-useractivitydisplayname-1') && !containsAny(toLower(event_name), 'delete group', 'add member', 'add eligible member', 'remove member', 'remove eligible member','user deleted security info') && InList(toLower(result), 'success') |