# Code Changes for microsoft-evsystem-str-service-state-modify-7036-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | host |  | ['({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{6}[\+\-]\d{1,2}:\d{1,2})(\s({host}[\w\-.]+)\s)?', 'Service Control Manager(\s+[^\s"]+){3}\s+({host}[\w.-]+)', '\w+\s\d+\s\d+:\d+:\d+\s({host}[^\s]+)\sMSWinEventLog'] |