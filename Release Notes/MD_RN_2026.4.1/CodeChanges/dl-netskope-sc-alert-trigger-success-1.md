# Code Changes for dl-netskope-sc-alert-trigger-success-1 (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression |  | InList(type, 'netskope-sc-json-alert-trigger-success-dlp_match_info')  && (!exists(alert_severity) || InList(toLower(alert_severity), 'unknown', 'low')) |