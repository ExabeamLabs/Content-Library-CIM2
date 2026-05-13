# Code Changes for microsoft-azure-file-permission-modify-fail (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression |  | InList(type, 'microsoft-azure-json-file-success-1', 'microsoft-azure-json-file-success-2') && containsAny(toLower(operation), 'setcontaineracl', 'sftpsetstat') && startsWithAny(result_code, '4') |