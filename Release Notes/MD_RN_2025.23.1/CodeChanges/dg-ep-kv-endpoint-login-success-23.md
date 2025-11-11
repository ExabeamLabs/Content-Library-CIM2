# Code Changes for dg-ep-kv-endpoint-login-success-23 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'domain', 'event_code', 'host', 'process_name', 'time', 'user'] |
| edit_regex_field | host |  | ['\sComputer_Name=\"([^\/\\\"]+[\\\/])?({dest_host}({host}[^\"]+))\"'] |
| added_regex_field | dest_host |  | ['\sComputer_Name=\"([^\/\\\"]+[\\\/])?({dest_host}({host}[^\"]+))\"'] |
| removed_attribute | DupFields |  | N/A |