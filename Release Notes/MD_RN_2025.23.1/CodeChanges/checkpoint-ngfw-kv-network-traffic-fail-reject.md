# Code Changes for checkpoint-ngfw-kv-network-traffic-fail-reject (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'dest_ip', 'dest_port', 'event_category', 'event_name', 'failure_reason', 'host', 'origin_ip', 'origin_name', 'protocol', 'src_ip', 'src_port', 'time'] |
| added_regex_field | event_name |  | ['action:"({event_name}[^"]+)'] |
| removed_attribute | DupFields |  | N/A |