# Code Changes for airlock-allowlisting-alert-trigger-success (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression |  | InList(type, 'airlock-allowlisting-json-alert-trigger-success-pprocess') && InList(toLower(operation_type), '2', '3','7','13', '14', '15') |