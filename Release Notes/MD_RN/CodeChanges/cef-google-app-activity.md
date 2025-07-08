# Code Changes for cef-google-app-activity (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | app | ['"applicationName":"({app}[^"]+)"', '"name":"app_name","value":"(unknown|({app}[^"]+?))\s*"'] | ['"applicationName":"({app}[^"]+)"', '"name":"app_name","value":"(unknown|({app}[^"]+?))\s*"', 'destinationServiceName=({app}[^=]+?)\s*(\w+=|$)'] |