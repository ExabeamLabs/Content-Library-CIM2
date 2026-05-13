# Code Changes for microsoft-azure-file-list-fail (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression |  | InList(type, 'microsoft-azure-json-file-success-1', 'microsoft-azure-json-file-success-2', 'microsoft-azuremon-json-file-storagecategory') && containsAny(toLower(operation), 'listblobs', 'listcontainers', 'listfiles','getpageranges', 'listshares', 'listqueues', 'sftpstat', 'sftpreaddir') && startsWithAny(result_code, '4') |