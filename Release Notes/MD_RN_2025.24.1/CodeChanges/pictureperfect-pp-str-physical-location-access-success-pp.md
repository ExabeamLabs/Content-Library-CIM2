# Code Changes for pictureperfect-pp-str-physical-location-access-success-pp (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['direction', 'first_name', 'last_name', 'location_door', 'location_full', 'time', 'user'] |
| edit_regex_field | location_full |  | ['^[^|]*?\|([^|]*\|){12}({location_door}({location_full}[^|]+))\|'] |
| added_regex_field | location_door |  | ['^[^|]*?\|([^|]*\|){12}({location_door}({location_full}[^|]+))\|'] |
| removed_attribute | DupFields |  | N/A |