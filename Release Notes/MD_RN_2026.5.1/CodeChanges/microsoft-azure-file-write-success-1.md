# Code Changes for microsoft-azure-file-write-success-1 (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression |  | InList(type, 'microsoft-azure-json-file-success-1', 'microsoft-azure-json-file-success-2') && containsAny(toLower(operation), 'putblob', 'copyblobdestination','copyblob','appendblock','putpage','putblocklist','putblock','leasefile','appendfile', 'sftpwrite') && !startsWithAny(result_code, '4') |