# Code Changes for microsoft-azure-file-write-fail (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression |  | InList(type, 'microsoft-azure-json-file-success-1', 'microsoft-azure-json-file-success-2') && containsAny(toLower(operation), 'putblob', 'copyblobdestination','copyblob','appendblock','putpage','putblocklist','putblock','appendfile','leasefile', 'sftpwrite') && startsWithAny(result_code, '4') |