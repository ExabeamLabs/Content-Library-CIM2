# Code Changes for infoblox-bddi-str-configuration-modify-success-transfersuccess (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'additional_info', 'host', 'operation', 'process_id', 'process_name', 'result', 'zone'] |
| edit_regex_field | action |  | ['Transfer status:\s({result}({action}[^\s]+?))\s*$'] |
| added_regex_field | result |  | ['Transfer status:\s({result}({action}[^\s]+?))\s*$'] |
| removed_attribute | DupFields |  | N/A |