# Code Changes for microsoft-windows-registry-delete-success-3 (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression |  | InList(type, 'microsoft-evsecurity-xml-registry-create-success-4657') && containsAny(toLower(operation), '1906', 'registry value deleted') |