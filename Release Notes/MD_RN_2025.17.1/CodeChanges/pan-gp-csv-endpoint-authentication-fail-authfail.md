# Code Changes for pan-gp-csv-endpoint-authentication-fail-authfail (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['device_name', 'domain', 'email_address', 'failure_reason', 'host', 'serial_num', 'service_name', 'src_host', 'src_ip', 'src_port', 'time', 'user', 'virtual_station_name'] |
| added_regex_field | virtual_station_name |  | [',SYSTEM,([^,]*,){3}({virtual_station_name}[^,]+?)\s*,'] |