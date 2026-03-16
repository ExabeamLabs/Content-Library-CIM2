# Code Changes for microsoft-evapp-str-endpoint-notification-1202 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | host |  | ['"Computer":"({host}[\w\.\-]+)"', '({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{6}[\+\-]\d{1,2}:\d{1,2})(\s({host}[\w\-.]+)\s)?', ':\d+\s({host}[^\s]+)\sMSWinEventLog', '\s({host}[\w.-]+)\s+[^"\s]+\s+Security policies were propagated with warning', 'exa_regex=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{6}[\+\-]\d{1,2}:\d{1,2})(\s({host}[\w\-.]+)\s)?'] |