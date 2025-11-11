# Code Changes for cef-azure-event-hub-cosmosdb (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['app', 'category', 'db_name', 'db_object', 'db_operation', 'event_hub_name', 'event_hub_namespace', 'host', 'object', 'resource', 'resource_id', 'src_ip', 'src_port', 'subscription_id', 'table_name', 'time', 'user', 'user_agent'] |
| edit_regex_field | object |  | ['"resourceId":\s*"({resource}({object}[^"]{1,249}))'] |
| added_regex_field | resource |  | ['"resourceId":\s*"({resource}({object}[^"]{1,249}))'] |
| removed_attribute | DupFields |  | N/A |