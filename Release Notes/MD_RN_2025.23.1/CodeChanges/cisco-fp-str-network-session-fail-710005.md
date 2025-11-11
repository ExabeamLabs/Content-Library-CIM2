# Code Changes for cisco-fp-str-network-session-fail-710005 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'dest_interface', 'dest_ip', 'dest_port', 'event_code', 'event_name', 'host', 'operation', 'priority', 'protocol', 'result', 'src_ip', 'src_port', 'time'] |
| edit_regex_field | action |  | ['({event_name}({protocol}TCP|UDP)\s+({action}request ({result}discarded)))', '({operation}({protocol}TCP|UDP)\s+({action}request ({result}discarded)))'] |
| edit_regex_field | protocol |  | ['({event_name}({protocol}TCP|UDP)\s+({action}request ({result}discarded)))', '({operation}({protocol}TCP|UDP)\s+({action}request ({result}discarded)))'] |
| edit_regex_field | result |  | ['({event_name}({protocol}TCP|UDP)\s+({action}request ({result}discarded)))', '({operation}({protocol}TCP|UDP)\s+({action}request ({result}discarded)))'] |
| added_regex_field | operation |  | ['({operation}({protocol}TCP|UDP)\s+({action}request ({result}discarded)))'] |
| removed_attribute | DupFields |  | N/A |