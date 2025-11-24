# Code Changes for lenel-physical-access (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['badge_id', 'employee_id', 'first_name', 'host', 'last_name', 'location_door', 'location_full', 'result', 'time'] |
| edit_regex_field | location_door |  | ['"READERDESC":\s*"({location_full}({location_door}[^"]+))'] |
| added_regex_field | location_full |  | ['"READERDESC":\s*"({location_full}({location_door}[^"]+))'] |
| removed_attribute | DupFields |  | N/A |