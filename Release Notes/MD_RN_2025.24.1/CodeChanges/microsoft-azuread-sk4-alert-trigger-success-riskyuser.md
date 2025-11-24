# Code Changes for microsoft-azuread-sk4-alert-trigger-success-riskyuser (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_type', 'app', 'category', 'email_user', 'event_category', 'event_name', 'first_name', 'last_name', 'operation', 'resource', 'resource_id', 'result', 'src_ip', 'time'] |
| edit_regex_field | category |  | ['Category":"({event_name}({category}[^"]+))'] |
| edit_regex_field | event_category |  | ['"Type":"({alert_type}({event_category}[^"]+))'] |
| added_regex_field | alert_type |  | ['"Type":"({alert_type}({event_category}[^"]+))'] |
| added_regex_field | event_name |  | ['Category":"({event_name}({category}[^"]+))'] |
| removed_attribute | DupFields |  | N/A |