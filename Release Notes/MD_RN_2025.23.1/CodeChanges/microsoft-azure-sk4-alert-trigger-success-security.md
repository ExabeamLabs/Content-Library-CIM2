# Code Changes for microsoft-azure-sk4-alert-trigger-success-security (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_id', 'action', 'additional_info', 'alert_id', 'alert_name', 'alert_severity', 'alert_type', 'app', 'azure_category', 'azure_resource_type', 'correlation_id', 'dest_host', 'domain', 'email_address', 'event_hub_name', 'event_hub_namespace', 'full_name', 'host', 'object', 'operation', 'resource', 'resource_group', 'resource_id', 'result', 'server', 'severity', 'src_host', 'src_ip', 'src_port', 'subscription_id', 'time', 'user', 'user_upn'] |
| edit_regex_field | alert_type |  | ['eventName":"({alert_name}({alert_type}[^"\\]+))[\\]*"'] |
| added_regex_field | alert_name |  | ['eventName":"({alert_name}({alert_type}[^"\\]+))[\\]*"'] |
| removed_attribute | DupFields |  | N/A |