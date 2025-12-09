# Code Changes for box-ccm-cef-file-success-contentaccess (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'access_type', 'app', 'bytes', 'email_address', 'file_dir', 'file_ext', 'file_name', 'file_type', 'full_name', 'operation', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | access |  | ['"+event_type"+:"+({operation}({access}[^"]+))"+'] |
| added_regex_field | operation |  | ['"+event_type"+:"+({operation}({access}[^"]+))"+'] |
| removed_attribute | DupFields |  | N/A |