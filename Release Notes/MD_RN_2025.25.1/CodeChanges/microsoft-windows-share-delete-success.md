# Code Changes for microsoft-windows-share-delete-success (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression |  | InList(type,'microsoft-evsecurity-xml-share-delete-success-5144', 'microsoft-evsecurity-cef-share-access-success-5144', 'microsoft-evsecurity-kv-share-access-success-5144','microsoft-evsecurity-sk4-share-delete-success-5144') |