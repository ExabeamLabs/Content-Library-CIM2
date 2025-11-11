# Code Changes for microsoft-mssql-kv-database-login-success-18453 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'domain', 'host', 'service_name', 'src_ip', 'time', 'user'] |
| edit_regex_field | host |  | ['\WComputerName=({dest_host}({host}[\w\-\.]+))\s*(\w+=|$)'] |
| added_regex_field | dest_host |  | ['\WComputerName=({dest_host}({host}[\w\-\.]+))\s*(\w+=|$)'] |
| removed_attribute | DupFields |  | N/A |