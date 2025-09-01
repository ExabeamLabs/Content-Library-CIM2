# Code Changes for dl-airlock-allowlisting-policy-modify-success (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression |  | InList(type, 'airlock-allowlisting-json-app-activity-success-task') && InList(toLower(event_name), 'policy modify') |