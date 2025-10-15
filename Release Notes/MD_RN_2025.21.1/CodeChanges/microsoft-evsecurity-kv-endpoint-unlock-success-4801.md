# Code Changes for microsoft-evsecurity-kv-endpoint-unlock-success-4801 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | dest_host |  | ['({dest_host}({host}[\w\-.]+))\s+ADAuditPlus', '\WCLIENT_HOST_NAME\s*=\s*(null|({dest_host}[\w\-.]+))'] |
| edit_regex_field | host |  | ['({dest_host}({host}[\w\-.]+))\s+ADAuditPlus'] |
| removed_attribute | DupFields |  | N/A |