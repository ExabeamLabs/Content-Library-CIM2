# Code Changes for microsoft-azure-cef-network-traffic-event (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'additional_info', 'app', 'category', 'dest_ip', 'dest_port', 'direction', 'email_address', 'email_domain', 'event_hub_name', 'event_hub_namespace', 'event_name', 'file_dir', 'file_name', 'file_path', 'host', 'object', 'operation', 'resource_id', 'result', 'rule', 'rule_id', 'src_host', 'src_ip', 'src_port', 'tenant_id', 'time', 'transaction_id', 'uri', 'user'] |
| edit_regex_field | operation |  | ['"operationName":"({event_name}({operation}[^"]+))"', '\Wact=({operation}[^=]+)\s+(\w+=|$)', '\WflexString1=({operation}[^=]+)\s+(\w+=|$)', 'category\":\"({operation}[^"]+)'] |
| added_regex_field | event_name |  | ['"operationName":"({event_name}({operation}[^"]+))"'] |
| removed_attribute | DupFields |  | N/A |