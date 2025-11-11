# Code Changes for pan-ngfw-cef-http-session-url-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'category', 'dest_interface', 'dest_ip', 'dest_network_zone', 'dest_port', 'dest_translated_ip', 'device_name', 'direction', 'domain', 'email_address', 'event_category', 'host', 'mime', 'network_app', 'protocol', 'serial_num', 'src_interface', 'src_ip', 'src_network_zone', 'src_port', 'src_translated_ip', 'time', 'uri_path', 'uri_query', 'url', 'user', 'web_domain'] |
| added_regex_field | device_name |  | ['\sdvchost=({device_name}[\w\-\.]+)'] |
| removed_attribute | DupFields |  | N/A |