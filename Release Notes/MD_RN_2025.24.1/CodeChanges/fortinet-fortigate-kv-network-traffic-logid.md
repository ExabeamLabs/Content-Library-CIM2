# Code Changes for fortinet-fortigate-kv-network-traffic-logid (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'additional_info', 'attack', 'attack_id', 'bytes', 'bytes_in', 'bytes_out', 'dest_country', 'dest_interface', 'dest_ip', 'dest_port', 'dest_role', 'dest_translated_ip', 'device_id', 'device_name', 'device_type', 'direction', 'domain', 'duration', 'email_address', 'event_id', 'event_name', 'host', 'more_info', 'network_app', 'os', 'os_version', 'packets_in', 'packets_out', 'policy_id', 'profile', 'protocol', 'result', 'result_reason', 'session_id', 'severity', 'src_country', 'src_host', 'src_interface', 'src_ip', 'src_mac', 'src_port', 'src_role', 'src_translated_ip', 'src_translated_port', 'subtype', 'time', 'tz', 'url', 'user', 'web_domain'] |
| edit_regex_field | additional_info |  | ['\smsg=\\?"?({additional_info}[^=]+?),?\\?"?\s*(\w+=|$)'] |
| added_regex_field | dest_role |  | ['\Wdstintfrole=\"+(undefined|({dest_role}[^\"]+))\"+'] |
| added_regex_field | src_role |  | ['\Wsrcintfrole=\"+(undefined|({src_role}[^\"]+))\"+'] |
| added_regex_field | web_domain |  | ['\Whostname="({web_domain}[^\"]+)"'] |