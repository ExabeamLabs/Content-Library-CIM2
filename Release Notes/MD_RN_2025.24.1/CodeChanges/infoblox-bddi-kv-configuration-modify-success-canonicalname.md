# Code Changes for infoblox-bddi-kv-configuration-modify-success-canonicalname (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['cname', 'event_name', 'host', 'operation', 'time'] |
| edit_regex_field | operation |  | ['({event_name}({operation}Created CnameRecord))'] |
| added_regex_field | event_name |  | ['({event_name}({operation}Created CnameRecord))'] |
| removed_attribute | DupFields |  | N/A |