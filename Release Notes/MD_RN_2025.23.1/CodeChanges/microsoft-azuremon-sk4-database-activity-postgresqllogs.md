# Code Changes for microsoft-azuremon-sk4-database-activity-postgresqllogs (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'app', 'category', 'cipher', 'db_operation', 'db_schema', 'domain', 'event_hub_name', 'event_hub_namespace', 'host', 'object', 'operation', 'protocol', 'resource', 'resource_id', 'server', 'server_group', 'subscription_id', 'table_name', 'time'] |
| edit_regex_field | additional_info |  | ['"detail":"({additional_info}[^"]+)', '"message":"({additional_info}({db_operation}[^"]+))'] |
| edit_regex_field | db_operation |  | ['"message":"({additional_info}({db_operation}[^"]+))'] |
| edit_regex_field | event_hub_namespace |  | ['Namespace:\s*(|({host}({event_hub_namespace}[^\]]+?)))\s*[\];]'] |
| edit_regex_field | object |  | ['"resourceId":\s*"({resource}({object}[^"]{1,249}))'] |
| added_regex_field | host |  | ['Namespace:\s*(|({host}({event_hub_namespace}[^\]]+?)))\s*[\];]'] |
| added_regex_field | resource |  | ['"resourceId":\s*"({resource}({object}[^"]{1,249}))'] |
| removed_attribute | DupFields |  | N/A |