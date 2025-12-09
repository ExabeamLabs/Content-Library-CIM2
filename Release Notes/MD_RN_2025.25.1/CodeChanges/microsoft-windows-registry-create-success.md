# Code Changes for microsoft-windows-registry-create-success (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression |  | InList(type,'microsoft-evsecurity-str-registry-create-success-4657') && containsAny(toLower(operation) , 'new registry value created') |