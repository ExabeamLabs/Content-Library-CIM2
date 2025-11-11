# Code Changes for microsoft-windows-xml-endpoint-notification-success-102 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'event_code', 'host', 'result', 'run_level', 'task_name', 'time'] |
| edit_regex_field | host |  | ['<Computer>({dest_host}({host}[\w.-]+))<\/Computer>'] |
| added_regex_field | dest_host |  | ['<Computer>({dest_host}({host}[\w.-]+))<\/Computer>'] |
| removed_attribute | DupFields |  | N/A |