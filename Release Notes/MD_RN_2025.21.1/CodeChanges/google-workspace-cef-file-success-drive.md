# Code Changes for google-workspace-cef-file-success-drive (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'app', 'category', 'dest_email_address', 'email_address', 'email_domain', 'file_dir', 'file_ext', 'file_id', 'file_name', 'file_owner', 'file_type', 'host', 'operation', 'privileges', 'service_name', 'src_file_dir', 'src_file_name', 'src_ip', 'src_port', 'time', 'user', 'user_id'] |
| edit_regex_field | access |  | ['"events":[^=]*?"name":"({operation}({access}[^"]+))"', '"events":[^=]*?"type":"access","name":"({operation}({access}[^"]+))"'] |
| added_regex_field | operation |  | ['"events":[^=]*?"name":"({operation}({access}[^"]+))"', '"events":[^=]*?"type":"access","name":"({operation}({access}[^"]+))"'] |
| removed_attribute | DupFields |  | N/A |