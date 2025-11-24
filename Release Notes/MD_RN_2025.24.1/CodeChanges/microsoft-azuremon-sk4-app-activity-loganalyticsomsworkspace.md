# Code Changes for microsoft-azuremon-sk4-app-activity-loganalyticsomsworkspace (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'additional_info', 'alert_name', 'alert_severity', 'app', 'cluster_name', 'computer_name', 'db_name', 'db_query', 'db_user', 'domain', 'error_code', 'event_category', 'event_code', 'event_name', 'group_name', 'host', 'object', 'operation', 'os', 'process_name', 'resource_id', 'response', 'result', 'result_code', 'server_name', 'session_id', 'src_ip', 'src_port', 'subscription_id', 'table', 'tenant_id', 'time', 'user', 'user_agent'] |
| edit_regex_field | resource_id |  | ['"_ResourceId":"({object}({resource_id}[^"]+))'] |
| added_regex_field | object |  | ['"_ResourceId":"({object}({resource_id}[^"]+))'] |
| removed_attribute | DupFields |  | N/A |