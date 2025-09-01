# Code Changes for microsoft-windows-registry-create-success-2 (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression |  | InList(type, 'microsoft-evsecurity-xml-registry-create-success-4657') && containsAny(toLower(operation), '1904', 'new registry value created') |