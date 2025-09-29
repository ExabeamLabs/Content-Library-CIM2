# Code Changes for dl-sentinelone-singularity-alert-trigger-success (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression |  | InList(type, 'sentinelone-singularityp-cef-alert-trigger-success-classification', 'sentinelone-singularityp-cef-alert-trigger-success-newactivethreat','sentinelone-singularityp-json-alert-trigger-success-url-1', 'sentinelone-singularityp-json-alert-trigger-success-activity_type') && (toLower(alert_name) = 'benign' || (!exists(alert_severity) && (!exists(category) || !InList(toLower(category), 'malicious', 'suspicious')) ) || InList(toLower(alert_severity), 'info', 'low', '0', '1', '2')) && !InList(toLower(alert_name), 'get','post','head','put','delete','options','patch') |