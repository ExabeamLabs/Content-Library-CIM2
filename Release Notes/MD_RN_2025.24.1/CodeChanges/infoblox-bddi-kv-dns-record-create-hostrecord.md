# Code Changes for infoblox-bddi-kv-dns-record-create-hostrecord (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['event_name', 'host', 'operation', 'time'] |
| edit_regex_field | operation |  | ['({event_name}({operation}Created HostRecord))'] |
| added_regex_field | event_name |  | ['({event_name}({operation}Created HostRecord))'] |
| removed_attribute | DupFields |  | N/A |