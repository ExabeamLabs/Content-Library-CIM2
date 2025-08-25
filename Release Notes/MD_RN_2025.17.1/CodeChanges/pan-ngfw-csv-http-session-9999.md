# Code Changes for pan-ngfw-csv-http-session-9999 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'alert_id', 'alert_name', 'alert_severity', 'alert_type', 'app', 'categories', 'category', 'dest_country', 'dest_domain', 'dest_email_address', 'dest_email_domain', 'dest_interface', 'dest_ip', 'dest_network_zone', 'dest_port', 'dest_translated_ip', 'dest_translated_port', 'dest_user', 'dest_user_full_name', 'device_name', 'direction', 'domain', 'email_address', 'email_domain', 'event_category', 'file_name', 'host', 'malware_file_name', 'malware_url', 'method', 'mime', 'network_app', 'protocol', 'referrer', 'result_code', 'rule', 'serial_num', 'session_id', 'severity', 'src_domain', 'src_interface', 'src_ip', 'src_location', 'src_network_zone', 'src_port', 'src_translated_ip', 'src_translated_port', 'src_user', 'threat_category', 'threat_id', 'time', 'uri_path', 'uri_query', 'url', 'user', 'user_agent', 'virtual_station_name', 'web_domain'] |
| removed_regex_field | result |  | [] |
| added_regex_field | result_code |  | [',THREAT,([^,]*,){24}({result_code}[^,]+?),'] |