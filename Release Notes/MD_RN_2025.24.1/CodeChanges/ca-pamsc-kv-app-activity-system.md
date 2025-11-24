# Code Changes for ca-pamsc-kv-app-activity-system (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['app', 'dest_host', 'dest_port', 'email_address', 'event_name', 'full_name', 'group_name', 'group_ou', 'host', 'protocol', 'src_ip', 'src_port', 'time', 'user', 'user_ou'] |
| edit_regex_field | dest_host |  | ['(?i)\sDevice Name\s*:\s*(?:\- \-|({host}({dest_host}[^,]+)))'] |
| added_regex_field | host |  | ['(?i)\sDevice Name\s*:\s*(?:\- \-|({host}({dest_host}[^,]+)))'] |
| removed_attribute | DupFields |  | N/A |