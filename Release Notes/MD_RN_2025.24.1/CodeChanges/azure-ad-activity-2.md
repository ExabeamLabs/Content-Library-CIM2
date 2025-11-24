# Code Changes for azure-ad-activity-2 (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'event_name', 'operation', 'provider_name', 'resource', 'resource_group', 'resource_id', 'subscription_id', 'time'] |
| edit_regex_field | operation |  | ['"operationName":\s*"({event_name}({operation}[^"]+))"'] |
| added_regex_field | event_name |  | ['"operationName":\s*"({event_name}({operation}[^"]+))"'] |
| removed_attribute | DupFields |  | N/A |