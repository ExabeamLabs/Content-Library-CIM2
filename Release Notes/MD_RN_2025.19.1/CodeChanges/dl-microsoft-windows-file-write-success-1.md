# Code Changes for dl-microsoft-windows-file-write-success-1 (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression |  | InList(type, 'microsoft-evsecurity-kv-file-fileoperation') and containsAny(toLower(operation),'write persisted key from file.','write persisted key to file.') |