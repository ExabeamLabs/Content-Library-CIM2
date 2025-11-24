# Code Changes for rubrik-events (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['alert_severity', 'dest_host', 'event_code', 'host', 'object', 'object_id', 'object_type', 'result', 'src_ip', 'src_port', 'time'] |
| edit_regex_field | host |  | ['nodeId="({dest_host}({host}[^"]+))"'] |
| added_regex_field | dest_host |  | ['nodeId="({dest_host}({host}[^"]+))"'] |
| removed_attribute | DupFields |  | N/A |