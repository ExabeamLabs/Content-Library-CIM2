# Code Changes for microsoft-azure-file-create-success-1 (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression |  | InList(type, 'microsoft-azuremon-json-file-storagecategory') && InList(toLower(operation), 'createfile', 'create') |