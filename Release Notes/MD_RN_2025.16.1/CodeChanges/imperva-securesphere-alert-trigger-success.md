# Code Changes for imperva-securesphere-alert-trigger-success (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression |  | InList(type, 'imperva-securesphere-cef-alert-trigger-success-servergroup', 'imperva-securesphere-kv-alert-trigger-success-catsecurity') && !containsAny(toLower(service_name),'http') && exists(alert_severity) && !InList(toLower(alert_severity), 'informative','unknown', 'low', 'info') |