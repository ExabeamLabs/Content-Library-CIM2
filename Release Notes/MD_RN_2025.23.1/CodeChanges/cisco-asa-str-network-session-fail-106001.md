# Code Changes for cisco-asa-str-network-session-fail-106001 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'dest_interface', 'dest_ip', 'dest_port', 'event_code', 'event_name', 'failure_reason', 'host', 'priority', 'protocol', 'result', 'src_host', 'src_ip', 'src_port', 'time'] |
| edit_regex_field | protocol |  | ['({event_name}Inbound ({protocol}\w+) connection ({result}denied))', '({failure_reason}Inbound ({protocol}\w+) connection ({result}denied))'] |
| edit_regex_field | result |  | ['({event_name}Inbound ({protocol}\w+) connection ({result}denied))', '({failure_reason}Inbound ({protocol}\w+) connection ({result}denied))'] |
| added_regex_field | failure_reason |  | ['({failure_reason}Inbound ({protocol}\w+) connection ({result}denied))'] |
| removed_attribute | DupFields |  | N/A |