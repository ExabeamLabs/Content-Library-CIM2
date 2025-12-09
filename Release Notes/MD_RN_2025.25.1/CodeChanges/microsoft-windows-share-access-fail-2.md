# Code Changes for microsoft-windows-share-access-fail-2 (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression |  | (InList(type, 'microsoft-evsecurity-json-share-access-hostname', 'microsoft-evsecurity-json-share-access-5145-1', 'microsoft-evsecurity-kv-share-access-success-5145', 'microsoft-evsecurity-sk4-share-access-success-5145', 'microsoft-evsecurity-json-share-access-success-5145', 'microsoft-evsecurity-kv-share-access-success-5145-2') and (exists(result) and !InList(ToLower(result), 'granted', '-', 'success', '授與', 'audit success', 'success audit', 'audit_success'))) |