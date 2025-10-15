# Code Changes for pan-ngfw-csv-network-traffic-success-allow (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'bytes', 'bytes_in', 'bytes_out', 'category', 'dest_country', 'dest_domain', 'dest_ip', 'dest_network_zone', 'dest_port', 'dest_translated_ip', 'dest_translated_port', 'dest_user', 'device_name', 'email_address', 'event_category', 'host', 'network_app', 'protocol', 'rule', 'session_id', 'src_country', 'src_domain', 'src_ip', 'src_network_zone', 'src_port', 'src_translated_ip', 'src_translated_port', 'src_user', 'subtype', 'time'] |
| edit_regex_field | host |  | [',TRAFFIC,([^,]*,){48}({device_name}({host}[\w.-]+))'] |
| edit_regex_field | time |  | [',((?:1969-[^,]+?)|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-]\d+:\d+)),', ',TRAFFIC,([^,]*,){2}({time}\d+-\d+-\d+T\d+:\d+:\d+\.\d+Z)', ',TRAFFIC,([^,]*,){2}({time}\d+\/\d+\/\d+\s+\d+:\d+:\d+)'] |
| added_regex_field | device_name |  | [',TRAFFIC,([^,]*,){48}({device_name}({host}[\w.-]+))'] |