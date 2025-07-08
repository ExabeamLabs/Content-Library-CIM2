# Code Changes for google-workspace-sk4-app-activity-success-admin (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | app | ['"applicationName":"({app}[^"]+)"', '"name":"app_name","value":"(unknown|({app}[^"]+?))\s*"'] | ['"applicationName":"({app}[^"]+)"', '"name":"app_name","value":"(unknown|({app}[^"]+?))\s*"', 'destinationServiceName=({app}[^=]+?)\s*(\w+=|$)'] |