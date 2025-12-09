# Code Changes for google-workspace-json-app-activity-success-groupsenterprise (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'app', 'email_address', 'email_domain', 'event_name', 'host', 'more_info', 'object', 'operation', 'privileges', 'resource_id', 'role_name', 'src_ip', 'src_port', 'tag', 'time', 'user', 'user_id'] |
| edit_regex_field | operation |  | ['"events":\[\{[^\[\]\{\}]*"name"\s*:\s*"({event_name}({operation}[^"]+))"'] |
| added_regex_field | event_name |  | ['"events":\[\{[^\[\]\{\}]*"name"\s*:\s*"({event_name}({operation}[^"]+))"'] |
| removed_attribute | DupFields |  | N/A |