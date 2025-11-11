# Code Changes for microsoft-evsecurity-kv-service-create-success-4622 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'event_code', 'event_id', 'event_name', 'host', 'result', 'service_name', 'time'] |
| edit_regex_field | host |  | ['ComputerName=({dest_host}({host}[\w\-\.]+))'] |
| added_regex_field | dest_host |  | ['ComputerName=({dest_host}({host}[\w\-\.]+))'] |
| removed_attribute | DupFields |  | N/A |