# Code Changes for citrix-cgateway-str-vpn-logout-success-icaend (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['bytes_in', 'bytes_out', 'dest_ip', 'dest_port', 'domain', 'duration', 'event_name', 'host', 'session_duration', 'source_connection_id', 'src_ip', 'src_port', 'time', 'user'] |
| added_regex_field | session_duration |  | ['\sDuration ({session_duration}\S+)'] |
| removed_attribute | DupFields |  | N/A |