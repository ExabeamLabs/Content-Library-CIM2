# Code Changes for microsoft-evsecurity-json-endpoint-notification-4627-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'login_type', 'time', 'user', 'user_sid'] |
| edit_regex_field | host |  | ['"computer":"({dest_host}({host}[^"]+))'] |
| added_regex_field | dest_host |  | ['"computer":"({dest_host}({host}[^"]+))'] |
| removed_attribute | DupFields |  | N/A |