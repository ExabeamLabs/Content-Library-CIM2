# Code Changes for microsoft-evsecurity-kv-policy-modify-4948 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'event_code', 'event_name', 'host', 'result', 'rule', 'rule_id', 'time'] |
| edit_regex_field | additional_info |  | ['Message=({event_name}({additional_info}[^\.]+))'] |
| added_regex_field | event_name |  | ['Message=({event_name}({additional_info}[^\.]+))'] |
| removed_attribute | DupFields |  | N/A |