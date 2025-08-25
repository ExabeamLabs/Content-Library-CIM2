# Code Changes for pan-ngfw-csv-configuration-modify-success-configfailed (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['asset_id', 'device_name', 'event_category', 'host', 'object', 'operation', 'result', 'serial_num', 'src_host', 'src_ip', 'time', 'user', 'virtual_station_name'] |
| added_regex_field | virtual_station_name |  | [',CONFIG,([^,]*,){4}({virtual_station_name}[^,]+?),'] |