# Code Changes for microsoft-evterminalservicesgateway-xml-endpoint-login-terminalservice-21 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | process_id |  | ['<Execution ProcessID\\*=(\'|")({process_id}\d+)(\'|")\s+ThreadID\\*=(\'|")({thread_id}\d+)(\'|")'] |
| edit_regex_field | thread_id |  | ['<Execution ProcessID\\*=(\'|")({process_id}\d+)(\'|")\s+ThreadID\\*=(\'|")({thread_id}\d+)(\'|")'] |