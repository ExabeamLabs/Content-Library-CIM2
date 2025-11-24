# Code Changes for ca-pamsc-csv-endpoint-login-fail-baduserid (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['app', 'dest_host', 'dest_port', 'email_address', 'event_name', 'failure_reason', 'full_name', 'group_name', 'group_ou', 'host', 'protocol', 'src_ip', 'src_port', 'time', 'user', 'user_ou'] |
| edit_regex_field | dest_host |  | ['(?i)\sDevice Name\s*:\s*(?:\- \-|({host}({dest_host}[^,]+)))'] |
| edit_regex_field | event_name |  | ['({failure_reason}({event_name}Bad User ID))', '\sDetails:[^;]*:\s+({event_name}[^;]+?)\s*(;|$)'] |
| added_regex_field | failure_reason |  | ['({failure_reason}({event_name}Bad User ID))', '\sDetails:[^;]*:\s+({failure_reason}[^;]+?)\s*(;|$)'] |
| added_regex_field | host |  | ['(?i)\sDevice Name\s*:\s*(?:\- \-|({host}({dest_host}[^,]+)))'] |
| removed_attribute | DupFields |  | N/A |