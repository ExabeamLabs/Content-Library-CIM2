# Code Changes for microsoft-azure-cef-alert-trigger-success-block (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | event_hub_namespace |  | ['Namespace:\s*({host}({event_hub_namespace}\S+))'] |
| edit_regex_field | host |  | ['"host":"({host}[\w\-.]+)', 'Namespace:\s*({host}({event_hub_namespace}\S+))'] |
| removed_attribute | DupFields |  | N/A |