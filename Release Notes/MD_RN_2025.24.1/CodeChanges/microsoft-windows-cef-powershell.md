# Code Changes for microsoft-windows-cef-powershell (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'alert_severity', 'app', 'bytes_in', 'bytes_out', 'class_id', 'cn1', 'cn2', 'cn3', 'cs1', 'cs2', 'cs3', 'cs4', 'cs5', 'cs6', 'dest_interface', 'dest_port', 'dest_translated_ip', 'dest_translated_port', 'device_facility', 'device_id', 'device_vendor', 'device_version', 'direction', 'dproc', 'dtz', 'event_category', 'event_code', 'event_name', 'file_name', 'file_path', 'file_type', 'flex_string2', 'group_name', 'process_id', 'process_name', 'protocol', 'request', 'result', 'result_reason', 'service_name', 'src_interface', 'src_port', 'src_translated_ip', 'src_translated_port', 'time', 'user_uid'] |
| removed_regex_field | dest_domain |  | [] |
| removed_regex_field | dest_ip |  | [] |
| edit_regex_field | dest_port |  | ['\sdpt=({dest_port}\d+)'] |
| removed_regex_field | src_domain |  | [] |
| removed_regex_field | user |  | [] |