# Code Changes for microsoft-azuremon-sk4-app-notification-applicationgatewayfirewalllog (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'additional_info', 'category', 'event_name', 'file_dir', 'file_ext', 'file_name', 'file_path', 'host', 'instance_id', 'operation', 'resource_id', 'rule', 'rule_id', 'rule_type', 'src_ip', 'src_port', 'time', 'uri_path', 'uri_query'] |
| edit_regex_field | operation |  | ['"operationName":\s*"({event_name}({operation}[^"]+))"'] |
| added_regex_field | event_name |  | ['"operationName":\s*"({event_name}({operation}[^"]+))"'] |
| removed_attribute | DupFields |  | N/A |