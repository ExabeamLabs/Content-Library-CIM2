# Code Changes for dl-netskope-sc-alert-trigger-success (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression |  | InList(type, 'netskope-sc-sk4-alert-trigger-success-dlp','netskope-sc-json-alert-trigger-success-dlp-1', 'netskope-sc-json-alert-trigger-success-dlp-2') && (!exists(alert_severity) || InList(toLower(alert_severity), 'unknown', 'low', 'informational')) |