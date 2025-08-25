# Code Changes for pan-ngfw-csv-app-notification-system (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['asset_id', 'device_name', 'event_category', 'event_code', 'event_name', 'event_subtype', 'host', 'object', 'serial_num', 'severity', 'time', 'virtual_station_name'] |
| added_regex_field | virtual_station_name |  | [',SYSTEM,([^,]*,){3}({virtual_station_name}[^,]+?)\s*,'] |