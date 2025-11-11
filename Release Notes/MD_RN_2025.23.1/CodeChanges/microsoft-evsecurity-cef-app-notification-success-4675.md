# Code Changes for microsoft-evsecurity-cef-app-notification-success-4675 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'dest_host', 'event_code', 'event_id', 'event_name', 'host', 'time', 'trust_type', 'user_sid'] |
| edit_regex_field | host |  | ['"computer":"({dest_host}({host}[\w\-.]+))'] |
| added_regex_field | dest_host |  | ['"computer":"({dest_host}({host}[\w\-.]+))'] |
| removed_attribute | DupFields |  | N/A |