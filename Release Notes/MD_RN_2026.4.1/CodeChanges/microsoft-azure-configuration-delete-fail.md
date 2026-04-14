# Code Changes for microsoft-azure-configuration-delete-fail (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression |  | InList(type, 'azure-azuread-json-app-activity-useractivitydisplayname', 'azure-azuread-json-app-activity-useractivitydisplayname-1') && containsAny(toLower(event_name), 'user deleted security info') && containsAny(toLower(result_reason), 'fail') |