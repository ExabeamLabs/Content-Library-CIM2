# Code Changes for microsoft-azuremon-json-endpoint-activity-success-catchall (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'process_command_line', 'provider_name', 'resource_group', 'resource_id', 'role', 'src_ip', 'src_port', 'subscription_id', 'time'] |
| edit_regex_field | src_ip |  | ['exa_json_path=$.CallerIpAddress,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})+)(:({src_port}\d+))?', 'exa_json_path=$.properties.IPAddress,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?'] |
| edit_regex_field | src_port |  | ['exa_json_path=$.CallerIpAddress,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})+)(:({src_port}\d+))?', 'exa_json_path=$.properties.IPAddress,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?'] |
| added_regex_field | action |  | ['exa_json_path=$.properties.RawEventData.authorization,exa_regex=[^\]]+action\\?"[^,]+?"({action}[^,]+?)\\?"'] |
| added_regex_field | role |  | ['exa_json_path=$.properties.RawEventData.authorization,exa_regex=[^\]]+role\\?"[^,]+?"({role}[^,]+?)\\?"'] |