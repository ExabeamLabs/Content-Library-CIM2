# Code Changes for infoblox-bddi-kv-dns-record-delete-success-mxrecord (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['event_name', 'host', 'operation', 'time'] |
| edit_regex_field | operation |  | ['({event_name}({operation}Deleted MxRecord))'] |
| added_regex_field | event_name |  | ['({event_name}({operation}Deleted MxRecord))'] |
| removed_attribute | DupFields |  | N/A |