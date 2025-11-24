# Code Changes for dl-pan-ngfw-alert-trigger-success-10 (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression |  | InList(type, 'pan-ngfw-mix-alert-trigger-success-virus', 'pan-ngfw-mix-alert-trigger-success-threatvulnerability', 'pan-ngfw-json-alert-trigger-success-vulnerability') && !InList(toLower(action), 'reset-both') && (!exists(alert_severity) || InList(toLower(alert_severity), 'informational', 'low')) |