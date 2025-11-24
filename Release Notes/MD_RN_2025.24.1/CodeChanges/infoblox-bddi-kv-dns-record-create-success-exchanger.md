# Code Changes for infoblox-bddi-kv-dns-record-create-success-exchanger (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['event_name', 'host', 'operation', 'priority', 'time'] |
| edit_regex_field | operation |  | ['({event_name}({operation}Created MxRecord))'] |
| added_regex_field | event_name |  | ['({event_name}({operation}Created MxRecord))'] |
| removed_attribute | DupFields |  | N/A |