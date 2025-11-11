# Code Changes for microsoft-evsecurity-kv-endpoint-notification-success-4780-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'dest_domain', 'dest_host', 'dest_user', 'domain', 'event_code', 'event_id', 'host', 'operation_type', 'result', 'time', 'user', 'user_sid'] |
| edit_regex_field | host |  | ['ComputerName\=({dest_host}({host}[\w\-.]+?))\s'] |
| added_regex_field | dest_host |  | ['ComputerName\=({dest_host}({host}[\w\-.]+?))\s'] |
| removed_attribute | DupFields |  | N/A |