# Code Changes for pan-ngfw-csv-network-traffic-success-allow (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'bytes', 'bytes_in', 'bytes_out', 'category', 'dest_country', 'dest_domain', 'dest_ip', 'dest_network_zone', 'dest_port', 'dest_translated_ip', 'dest_translated_port', 'dest_user', 'device_name', 'email_address', 'event_category', 'host', 'network_app', 'protocol', 'rule', 'session_id', 'src_country', 'src_domain', 'src_ip', 'src_network_zone', 'src_port', 'src_translated_ip', 'src_translated_port', 'src_user', 'subtype', 'time', 'user'] |
| edit_regex_field | email_address |  | ['TRAFFIC,([^,]*,){8}\s*(({email_address}[^@,]+@[^\.]+\.[^,]+)|(?:({src_domain}[^\s,\\]+)\\)?({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))),'] |
| edit_regex_field | src_domain |  | ['TRAFFIC,([^,]*,){8}\s*(({email_address}[^@,]+@[^\.]+\.[^,]+)|(?:({src_domain}[^\s,\\]+)\\)?({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))),'] |
| edit_regex_field | src_user |  | ['TRAFFIC,([^,]*,){8}\s*(({email_address}[^@,]+@[^\.]+\.[^,]+)|(?:({src_domain}[^\s,\\]+)\\)?({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))),'] |
| added_regex_field | user |  | ['TRAFFIC,([^,]*,){8}\s*(({email_address}[^@,]+@[^\.]+\.[^,]+)|(?:({src_domain}[^\s,\\]+)\\)?({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))),'] |
| removed_attribute | DupFields |  | N/A |