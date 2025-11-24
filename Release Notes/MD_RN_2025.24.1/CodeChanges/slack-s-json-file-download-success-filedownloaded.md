# Code Changes for slack-s-json-file-download-success-filedownloaded (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'dest_host', 'dest_ip', 'dest_port', 'domain', 'email_address', 'email_domain', 'file_type', 'full_name', 'operation', 'src_file_ext', 'src_file_name', 'time', 'user_agent', 'user_id'] |
| edit_regex_field | operation |  | ['"action":\s*"({access}({operation}[^"]+))'] |
| added_regex_field | access |  | ['"action":\s*"({access}({operation}[^"]+))'] |
| removed_attribute | DupFields |  | N/A |