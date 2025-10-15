# Code Changes for box-ccm-json-file-activity-success-event (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'access_type', 'additional_info', 'app', 'bytes', 'dest_email_address', 'dest_email_domain', 'dest_host', 'dest_user', 'dest_user_full_name', 'email_address', 'email_domain', 'file_dir', 'file_ext', 'file_name', 'file_type', 'folder_name', 'full_name', 'host', 'operation', 'permission', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | access |  | ['[^\w]event_type"+\s*:\s*"+({operation}({access}[^",]+))[",\]\}]'] |
| edit_regex_field | host |  | ['\d+:\d+ ({dest_host}({host}[^\s]+)) \{'] |
| added_regex_field | dest_host |  | ['\d+:\d+ ({dest_host}({host}[^\s]+)) \{'] |
| added_regex_field | operation |  | ['[^\w]event_type"+\s*:\s*"+({operation}({access}[^",]+))[",\]\}]'] |
| removed_attribute | DupFields |  | N/A |