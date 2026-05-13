# Code Changes for microsoft-azure-file-read-success-2 (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression |  | InList(type, 'microsoft-azure-json-file-success-1', 'microsoft-azure-json-file-success-2') && containsAny(toLower(operation), 'getblob', 'copyblobsource','readfile','getpathstatus', 'sftpread', 'sftpreaddir', 'sftpopen') && !containsAny(toLower(operation), 'properties', 'metadata', 'tag') && !startsWithAny(result_code, '4') |