# Code Changes for cisco-fp-str-network-session-fail-710003 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'dest_interface', 'dest_ip', 'dest_port', 'event_code', 'event_name', 'failure_reason', 'host', 'operation', 'priority', 'protocol', 'src_host', 'src_ip', 'src_port', 'time'] |
| edit_regex_field | failure_reason |  | ['({failure_reason}({protocol}\S+?) ({event_name}access denied by ACL))', '({failure_reason}({protocol}\S+?) ({operation}access denied by ACL))'] |
| edit_regex_field | protocol |  | ['({failure_reason}({protocol}\S+?) ({event_name}access denied by ACL))', '({failure_reason}({protocol}\S+?) ({operation}access denied by ACL))'] |
| added_regex_field | operation |  | ['({failure_reason}({protocol}\S+?) ({operation}access denied by ACL))'] |
| removed_attribute | DupFields |  | N/A |