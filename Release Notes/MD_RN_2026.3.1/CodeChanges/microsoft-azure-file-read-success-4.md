# Code Changes for microsoft-azure-file-read-success-4 (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression |  | InList(type, 'microsoft-azuremon-json-file-storagecategory') && InList(toLower(operation), 'getfile', 'read') |