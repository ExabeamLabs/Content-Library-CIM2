# Code Changes for microsoft-evsystem-str-endpoint-authentication-fail-5723 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | host |  | ['({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{6}[\+\-]\d{1,2}:\d{1,2})(\s({host}[\w\-.]+)\s)?', ':\d+\s({host}[^\s]+)\sMSWinEventLog', '\s({host}[\w.-]+)\s+[^\s"]+\s+The session setup from computer'] |