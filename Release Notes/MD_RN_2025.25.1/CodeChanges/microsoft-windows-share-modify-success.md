# Code Changes for microsoft-windows-share-modify-success (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression |  | InList(type, 'microsoft-evsecurity-kv-share-modify-success-5143', 'microsoft-evsecurity-json-share-modify-success-5143', 'microsoft-evsecurity-cef-share-access-success-5143', 'microsoft-evsecurity-kv-share-access-success-5143','microsoft-evsecurity-xml-share-modify-success-5143','microsoft-evsecurity-sk4-share-modify-success-5143') and (!exists(result) or InList(ToLower(result), 'granted', '-', 'success', 'audit success','success audit', '0x8020000000000000')) |