# Code Changes for microsoft-azure-sk4-app-activity-userupdate (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'app', 'category', 'dest_email_address', 'dest_user', 'email_address', 'event_category', 'event_name', 'object', 'operation', 'provider_name', 'resource', 'resource_group', 'resource_id', 'result', 'src_ip', 'src_port', 'subscription_id', 'time', 'user_agent'] |
| edit_regex_field | event_name |  | ['"ActivityDisplayName":\s*"({operation}({event_name}[^"]+))"'] |
| added_regex_field | operation |  | ['"ActivityDisplayName":\s*"({operation}({event_name}[^"]+))"'] |
| removed_attribute | DupFields |  | N/A |