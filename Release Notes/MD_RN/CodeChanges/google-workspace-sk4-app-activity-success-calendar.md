# Code Changes for google-workspace-sk4-app-activity-success-calendar (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | app | ['"applicationName":"({app}[^"]+)"', '"name":"app_name","value":"(unknown|({app}[^"]+?))\s*"', '({app}calendar)'] | ['"applicationName":"({app}[^"]+)"', '"name":"app_name","value":"(unknown|({app}[^"]+?))\s*"', '({app}calendar)', 'destinationServiceName=({app}[^=]+?)\s*(\w+=|$)'] |