# Code Changes for microsoft-azure-cef-network-traffic-firewall (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'additional_info', 'app', 'category', 'direction', 'email_address', 'email_domain', 'event_hub_name', 'event_hub_namespace', 'file_dir', 'file_name', 'file_path', 'host', 'instance_id', 'object', 'operation', 'provider_name', 'resource_group', 'resource_id', 'result', 'rule', 'rule_id', 'src_host', 'src_ip', 'src_port', 'subscription_id', 'tenant_id', 'time', 'transaction_id', 'uri', 'user'] |
| added_regex_field | tenant_id |  | ['"tenantId"\s*:\s*"({tenant_id}[^"]+)'] |