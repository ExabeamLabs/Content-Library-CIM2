# Code Changes for dl-exabeam-nganalytics-rule-trigger-success (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression |  | InList(type, 'exabeam-nganalytics-json-rule-trigger-success-nganalytics' ) && toLower(operation_type)='rule-trigger' |