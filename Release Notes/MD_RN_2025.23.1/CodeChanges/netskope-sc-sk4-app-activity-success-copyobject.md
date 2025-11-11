# Code Changes for netskope-sc-sk4-app-activity-success-copyobject (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'action', 'app', 'auth_method', 'browser', 'bytes', 'dest_ip', 'dest_port', 'domain', 'email_address', 'email_domain', 'file_dir', 'file_ext', 'file_name', 'file_type', 'folder_name', 'full_name', 'location', 'mime', 'object', 'object_type', 'operation', 'os', 'referrer', 'src_host', 'src_ip', 'src_port', 'time', 'url', 'user', 'user_agent', 'web_domain'] |
| edit_regex_field | file_type |  | ['"file_type":\s*"({mime}({file_type}[^"]+))'] |
| edit_regex_field | operation |  | ['"activity":\s*"({access}({operation}[^\"]+))'] |
| added_regex_field | access |  | ['"activity":\s*"({access}({operation}[^\"]+))'] |
| added_regex_field | mime |  | ['"file_type":\s*"({mime}({file_type}[^"]+))'] |
| removed_attribute | DupFields |  | N/A |