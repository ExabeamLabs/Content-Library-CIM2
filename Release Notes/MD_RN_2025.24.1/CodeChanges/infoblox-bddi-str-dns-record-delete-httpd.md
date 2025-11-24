# Code Changes for infoblox-bddi-str-dns-record-delete-httpd (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['event_name', 'host', 'operation', 'process_id', 'process_name', 'time'] |
| edit_regex_field | operation |  | ['({event_name}({operation}Deleted HostRecord))'] |
| added_regex_field | event_name |  | ['({event_name}({operation}Deleted HostRecord))'] |
| removed_attribute | DupFields |  | N/A |