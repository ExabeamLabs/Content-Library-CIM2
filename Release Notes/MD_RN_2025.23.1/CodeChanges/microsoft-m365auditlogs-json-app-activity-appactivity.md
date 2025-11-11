# Code Changes for microsoft-m365auditlogs-json-app-activity-appactivity (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'app', 'category', 'email_address', 'event_name', 'object_id', 'object_type', 'operation', 'resource', 'result', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | category |  | ['"category":"({resource}({category}[^"]+))"'] |
| edit_regex_field | operation |  | ['"activity":"({event_name}({operation}[^"]+))"'] |
| added_regex_field | event_name |  | ['"activity":"({event_name}({operation}[^"]+))"'] |
| added_regex_field | resource |  | ['"category":"({resource}({category}[^"]+))"'] |
| removed_attribute | DupFields |  | N/A |