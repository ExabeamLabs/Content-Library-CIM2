# Code Changes for microsoft-azuremon-sk4-app-activity-loganalyticsomsworkspace (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'additional_info', 'alert_name', 'alert_severity', 'app', 'cluster_name', 'computer_name', 'db_name', 'db_query', 'db_user', 'domain', 'error_code', 'event_category', 'event_code', 'event_name', 'group_name', 'host', 'operation', 'os', 'process_name', 'resource_id', 'response', 'result', 'result_code', 'server_name', 'session_id', 'src_ip', 'src_port', 'subscription_id', 'table', 'tenant_id', 'time', 'user', 'user_agent'] |
| edit_regex_field | host |  | ['"(H|h)ost(N|n)ame_s":"({host}[^"]+)', '"Computer":"({host}[^"]+)', '"Hostname_s":"({host}[^"]+)', '"host_name_s":"({host}[^"]+)"'] |
| edit_regex_field | src_ip |  | ['"client_ip_s":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?', '"sourceIPs":\["({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"'] |
| edit_regex_field | src_port |  | ['"client_ip_s":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?', '"sourceIPs":\["({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"'] |
| added_regex_field | action |  | ['"action_name_s":"({action}[^"]+)"'] |
| added_regex_field | db_name |  | ['"database_name_s":"({db_name}[^"]+)"'] |
| added_regex_field | db_query |  | ['"statement_s":"({db_query}[^"]+)"'] |
| added_regex_field | db_user |  | ['"database_principal_name_s":"({db_user}[^"]+)"'] |
| added_regex_field | response |  | ['"response_rows_d":"({response}[^"]+)"'] |
| added_regex_field | result |  | ['"succeeded_s":"({result}[^"]+)"'] |
| added_regex_field | server_name |  | ['"LogicalServerName_s":"({server_name}[^",]+)"'] |
| added_regex_field | session_id |  | ['"session_server_principal_name_s":"({session_id}[^"]+)"'] |