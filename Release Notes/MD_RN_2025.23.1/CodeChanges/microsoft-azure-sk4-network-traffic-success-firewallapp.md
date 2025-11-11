# Code Changes for microsoft-azure-sk4-network-traffic-success-firewallapp (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'additional_info', 'app', 'category', 'dest_host', 'dest_ip', 'dest_port', 'event_hub_name', 'event_hub_namespace', 'event_name', 'operation', 'policy_name', 'protocol', 'provider_name', 'resource', 'resource_group', 'resource_id', 'result', 'rule', 'src_ip', 'src_port', 'subscription_id', 'time'] |
| edit_regex_field | category |  | ['"({event_name}({category}AzureFirewallApplicationRule))"'] |
| edit_regex_field | result |  | ['Action:\s({action}({result}Allow))'] |
| added_regex_field | action |  | ['Action:\s({action}({result}Allow))'] |
| added_regex_field | event_name |  | ['"({event_name}({category}AzureFirewallApplicationRule))"'] |
| removed_attribute | DupFields |  | N/A |