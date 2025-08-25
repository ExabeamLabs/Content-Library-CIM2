# Code Changes for google-workspace-json-app-activity-success-groupsenterprise (Parser)

| Code Change | Field Name | 2025.11.1 | 2025.12.1 |
|-------------|------------|-----------|------------|
| edit_regex_field | app | ['"applicationName":"({app}[^"]+)"', '"name":"app_name","value":"(unknown|({app}[^"]+?))\s*"'] | ['"applicationName":"({app}[^"]+)"', '"name":"app_name","value":"(unknown|({app}[^"]+?))\s*"', 'destinationServiceName=({app}[^=]+?)\s*(\w+=|$)'] |