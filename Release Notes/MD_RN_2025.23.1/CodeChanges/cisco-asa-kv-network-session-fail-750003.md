# Code Changes for cisco-asa-kv-network-session-fail-750003 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'dest_ip', 'dest_port', 'event_code', 'event_name', 'failure_reason', 'host', 'priority', 'protocol', 'result_reason', 'src_host', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | result_reason |  | ['ERROR:\s*(|({failure_reason}({result_reason}.*?)))\s*$'] |
| added_regex_field | failure_reason |  | ['ERROR:\s*(|({failure_reason}({result_reason}.*?)))\s*$'] |
| removed_attribute | DupFields |  | N/A |