# Code Changes for infoblox-bddi-kv-dns-record-create-httpd (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['event_name', 'host', 'operation', 'server', 'time'] |
| edit_regex_field | operation |  | ['({event_name}({operation}Created HostAddress))'] |
| added_regex_field | event_name |  | ['({event_name}({operation}Created HostAddress))'] |
| removed_attribute | DupFields |  | N/A |