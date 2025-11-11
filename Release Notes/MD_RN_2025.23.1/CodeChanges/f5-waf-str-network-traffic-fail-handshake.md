# Code Changes for f5-waf-str-network-traffic-fail-handshake (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_ip', 'dest_port', 'event_name', 'failure_reason', 'host', 'protocol', 'src_ip', 'src_port'] |
| edit_regex_field | event_name |  | ['({failure_reason}({event_name}SSL Handshake failed))'] |
| added_regex_field | failure_reason |  | ['({failure_reason}({event_name}SSL Handshake failed))'] |
| removed_attribute | DupFields |  | N/A |