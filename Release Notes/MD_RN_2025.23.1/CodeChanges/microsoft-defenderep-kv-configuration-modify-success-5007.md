# Code Changes for microsoft-defenderep-kv-configuration-modify-success-5007 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'event_code', 'event_name', 'host', 'user_sid'] |
| edit_regex_field | additional_info |  | ['Message=({event_name}({additional_info}[^\.]+))\.'] |
| added_regex_field | event_name |  | ['Message=({event_name}({additional_info}[^\.]+))\.'] |
| removed_attribute | DupFields |  | N/A |