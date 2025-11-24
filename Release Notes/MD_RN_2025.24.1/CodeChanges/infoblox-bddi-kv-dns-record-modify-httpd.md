# Code Changes for infoblox-bddi-kv-dns-record-modify-httpd (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['event_name', 'host', 'operation', 'time'] |
| edit_regex_field | operation |  | ['({event_name}({operation}Modified HostRecord))'] |
| added_regex_field | event_name |  | ['({event_name}({operation}Modified HostRecord))'] |
| removed_attribute | DupFields |  | N/A |