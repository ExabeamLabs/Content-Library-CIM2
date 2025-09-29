# Code Changes for dl-microsoft-windows-log-enable-success (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression |  | InList(type, 'microsoft-sysmon-json-log-4','microsoft-sysmon-xml-log-4', 'microsoft-sysmon-cef-log-success-servicestatechanged') && toLower(service_state)='started' |