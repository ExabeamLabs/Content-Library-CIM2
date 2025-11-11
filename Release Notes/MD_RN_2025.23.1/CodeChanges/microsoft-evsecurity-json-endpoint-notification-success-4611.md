# Code Changes for microsoft-evsecurity-json-endpoint-notification-success-4611 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['auth_process', 'dest_host', 'domain', 'event_code', 'host', 'login_id', 'time', 'user', 'user_sid'] |
| edit_regex_field | host |  | ['Computer : ({dest_host}({host}[\w\-.]+))'] |
| added_regex_field | dest_host |  | ['Computer : ({dest_host}({host}[\w\-.]+))'] |
| removed_attribute | DupFields |  | N/A |