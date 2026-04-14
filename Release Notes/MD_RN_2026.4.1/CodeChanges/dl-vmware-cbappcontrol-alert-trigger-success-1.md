# Code Changes for dl-vmware-cbappcontrol-alert-trigger-success-1 (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression |  | InList(type, 'vmware-carbonblackappctrl-kv-alert-trigger-success-execution-1') && (!exists(alert_severity) || InList(toLower(alert_severity), 'info', 'low', '4', '5') || InList(toLower(alert_name), 'block unanalyzed scripts and executables')) |