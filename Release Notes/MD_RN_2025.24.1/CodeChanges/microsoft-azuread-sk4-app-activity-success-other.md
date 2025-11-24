# Code Changes for microsoft-azuread-sk4-app-activity-success-other (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'app', 'category', 'event_category', 'event_name', 'object', 'operation', 'resource', 'resource_id', 'src_ip', 'time'] |
| edit_regex_field | category |  | ['({category}ProvisioningManagement)', 'Category":\s*"({event_name}({category}[^"]+))'] |
| edit_regex_field | resource |  | ['"Resource":\s*"({object}({resource}[^"]+))'] |
| added_regex_field | event_name |  | ['Category":\s*"({event_name}({category}[^"]+))'] |
| added_regex_field | object |  | ['"Resource":\s*"({object}({resource}[^"]+))'] |
| removed_attribute | DupFields |  | N/A |