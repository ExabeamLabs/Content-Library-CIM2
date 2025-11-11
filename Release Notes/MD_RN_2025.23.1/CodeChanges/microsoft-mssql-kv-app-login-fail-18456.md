# Code Changes for microsoft-mssql-kv-app-login-fail-18456 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['app', 'dest_host', 'domain', 'event_code', 'event_name', 'failure_reason', 'host', 'service_name', 'src_host', 'src_ip', 'time', 'user'] |
| edit_regex_field | host |  | ['(\\n|\W)ComputerName=({dest_host}({host}[\w\-\.]+))\s*(\\n)?(\w+=|$)'] |
| added_regex_field | dest_host |  | ['(\\n|\W)ComputerName=({dest_host}({host}[\w\-\.]+))\s*(\\n)?(\w+=|$)'] |
| removed_attribute | DupFields |  | N/A |