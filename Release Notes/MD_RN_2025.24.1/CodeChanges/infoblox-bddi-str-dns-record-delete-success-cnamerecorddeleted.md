# Code Changes for infoblox-bddi-str-dns-record-delete-success-cnamerecorddeleted (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['event_name', 'host', 'operation', 'time'] |
| edit_regex_field | operation |  | ['({event_name}({operation}Deleted CnameRecord))'] |
| added_regex_field | event_name |  | ['({event_name}({operation}Deleted CnameRecord))'] |
| removed_attribute | DupFields |  | N/A |