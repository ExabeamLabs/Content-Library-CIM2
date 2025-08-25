# Code Changes for vmware-cbappcontrol-alert-trigger-success-4 (Event Builder)

| Code Change | Field Name | 2025.13.1 | 2025.14.1 |
|-------------|------------|-----------|------------|
| edit_conditions | expression | InList(type 'vmware-carbonblackappctrl-cef-alert-trigger-success-securityplatform') && exists(access) && containsAny(toLower(access), 'file', 'execution') && exists(alert_severity) && !InList(toLower(alert_severity), 'info', 'low', '4', '5') | InList(type, 'vmware-carbonblackappctrl-cef-alert-trigger-success-securityplatform') && exists(access) && containsAny(toLower(access), 'file', 'execution') && exists(alert_severity) && !InList(toLower(alert_severity), 'info', 'low', '4', '5') |