# Code Changes for rubrik-cdm-kv-app-logout-audit (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['alert_severity', 'dest_host', 'dest_ip', 'dest_port', 'event_name', 'host', 'object', 'object_id', 'object_type', 'result', 'time', 'user'] |
| edit_regex_field | host |  | ['nodeId="({dest_host}({host}[^"]+))"'] |
| added_regex_field | dest_host |  | ['nodeId="({dest_host}({host}[^"]+))"'] |
| removed_attribute | DupFields |  | N/A |