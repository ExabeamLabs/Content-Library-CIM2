# Code Changes for netskope-sc-alert-trigger-success-3 (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression |  | InList(type, 'netskope-sc-json-alert-trigger-success-yes','netskope-sc-json-alert-trigger-success-alertname', 'netskope-sc-json-alert-trigger-success-alertyes') && !InList(toLower(alert_type), 'dlp','device') && exists(alert_severity) && !InList(toLower(alert_severity), 'low','unknown','0', 'informational') |