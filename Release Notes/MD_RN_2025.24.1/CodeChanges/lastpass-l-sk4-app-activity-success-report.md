# Code Changes for lastpass-l-sk4-app-activity-success-report (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'action', 'additional_info', 'app', 'dest_email_address', 'dest_email_domain', 'dest_user', 'email_address', 'email_domain', 'event_name', 'file_name', 'file_type', 'operation', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | event_name |  | ['"+Action"+:"+({operation}({event_name}[^"]+))"+'] |
| added_regex_field | operation |  | ['"+Action"+:"+({operation}({event_name}[^"]+))"+'] |
| removed_attribute | DupFields |  | N/A |