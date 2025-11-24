# Code Changes for gtb-gtbdlp-cef-file-write-loggedviolation (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'alert_name', 'alert_severity', 'alert_type', 'dest_host', 'device_id', 'device_type', 'email_address', 'event_name', 'file_dir', 'file_ext', 'file_name', 'file_path', 'first_name', 'full_name', 'host', 'last_name', 'operation', 'src_file_dir', 'src_file_ext', 'src_file_name', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | operation |  | ['\Woperation=({event_name}({operation}[^=]+))\s+\w+='] |
| added_regex_field | event_name |  | ['\Woperation=({event_name}({operation}[^=]+))\s+\w+='] |
| removed_attribute | DupFields |  | N/A |