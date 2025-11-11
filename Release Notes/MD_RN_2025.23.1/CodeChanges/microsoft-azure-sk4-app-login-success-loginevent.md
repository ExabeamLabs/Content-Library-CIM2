# Code Changes for microsoft-azure-sk4-app-login-success-loginevent (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | event_hub_name |  | ['\[Namespace:\s*({host}({event_hub_namespace}\S+)) ; EventHub name:\s*({event_hub_name}[\w-]+)'] |
| edit_regex_field | event_hub_namespace |  | ['\[Namespace:\s*({host}({event_hub_namespace}\S+)) ; EventHub name:\s*({event_hub_name}[\w-]+)'] |
| edit_regex_field | host |  | ['"loginServer":"({host}[^",]+)', '\[Namespace:\s*({host}({event_hub_namespace}\S+)) ; EventHub name:\s*({event_hub_name}[\w-]+)'] |
| removed_attribute | DupFields |  | N/A |