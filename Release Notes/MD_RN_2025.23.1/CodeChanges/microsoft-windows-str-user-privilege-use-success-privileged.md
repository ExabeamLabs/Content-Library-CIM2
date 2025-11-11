# Code Changes for microsoft-windows-str-user-privilege-use-success-privileged (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['debug_privilege', 'dest_host', 'domain', 'environment_privilege', 'event_code', 'event_name', 'host', 'login_id', 'object_server', 'ownership_privilege', 'privileges', 'result', 'tcb_privilege', 'time', 'user'] |
| edit_regex_field | host |  | ['\s+(Information|Audit Success|Success Audit)\s+({dest_host}({host}[\w\-.]+))'] |
| added_regex_field | dest_host |  | ['\s+(Information|Audit Success|Success Audit)\s+({dest_host}({host}[\w\-.]+))'] |
| removed_attribute | DupFields |  | N/A |