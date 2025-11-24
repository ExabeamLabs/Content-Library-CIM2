# Code Changes for questsoftware-caad-cef-app-activity-appactivity (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'domain', 'email_address', 'event_name', 'host', 'operation', 'result', 'src_ip', 'src_port', 'time', 'user', 'user_sid'] |
| edit_regex_field | event_name |  | ['event=({operation}({event_name}[^=]+?))\s\w+='] |
| added_regex_field | operation |  | ['event=({operation}({event_name}[^=]+?))\s\w+='] |
| removed_attribute | DupFields |  | N/A |