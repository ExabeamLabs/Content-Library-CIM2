# Code Changes for cisco-asa-str-ip-assign-fail-737034 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['event_code', 'event_name', 'failure_reason', 'host', 'priority', 'session_id', 'time'] |
| added_regex_field | failure_reason |  | ['IPv(4|6) address:\s*({failure_reason}[^,]+?)\s*("*,|$)'] |
| removed_attribute | DupFields |  | N/A |