# Code Changes for google-workspace-sk4-app-activity-success-calendar (Parser)

| Code Change | Field Name | 2025.11.1 | 2025.12.1 |
|-------------|------------|-----------|------------|
| edit_regex_field | app | ['"applicationName":"({app}[^"]+)"', '"name":"app_name","value":"(unknown|({app}[^"]+?))\s*"', '({app}calendar)'] | ['"applicationName":"({app}[^"]+)"', '"name":"app_name","value":"(unknown|({app}[^"]+?))\s*"', '({app}calendar)', 'destinationServiceName=({app}[^=]+?)\s*(\w+=|$)'] |