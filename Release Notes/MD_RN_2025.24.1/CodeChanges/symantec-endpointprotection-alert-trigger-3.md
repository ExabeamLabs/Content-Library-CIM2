# Code Changes for symantec-endpointprotection-alert-trigger-3 (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression |  | InList(type,'symantec-endpointprotection-kv-alert-trigger-success-scanningyourcomputer', 'symantec-endpointprotection-kv-alert-trigger-success-denialofservice', 'symantec-endpointprotection-json-alert-trigger-success-firewallnetworkdetection', 'symantec-endpointprotection-json-alert-trigger-success-networkips') && exists(alert_severity) && !containsAny(toLower(alert_severity),'4','info', 'low', '67', '68', '69', '70', '71') |