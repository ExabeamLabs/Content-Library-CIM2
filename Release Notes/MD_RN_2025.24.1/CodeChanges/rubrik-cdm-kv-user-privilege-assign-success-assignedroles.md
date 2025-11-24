# Code Changes for rubrik-cdm-kv-user-privilege-assign-success-assignedroles (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['alert_severity', 'dest_host', 'event_code', 'host', 'object', 'object_id', 'object_type', 'operation', 'privileges', 'result', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | host |  | ['nodeId="({dest_host}({host}[^"]+))"'] |
| added_regex_field | dest_host |  | ['nodeId="({dest_host}({host}[^"]+))"'] |
| removed_attribute | DupFields |  | N/A |