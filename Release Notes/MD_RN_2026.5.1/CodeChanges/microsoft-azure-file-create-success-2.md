# Code Changes for microsoft-azure-file-create-success-2 (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression |  | InList(type, 'microsoft-azure-json-file-success-1', 'microsoft-azure-json-file-success-2') && containsAny(toLower(operation),'createpathfile', 'sftpcreate') && !startsWithAny(result_code, '4') |