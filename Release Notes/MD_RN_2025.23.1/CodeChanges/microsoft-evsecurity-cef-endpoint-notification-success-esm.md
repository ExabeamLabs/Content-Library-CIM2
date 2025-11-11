# Code Changes for microsoft-evsecurity-cef-endpoint-notification-success-esm (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'domain', 'event_code', 'host', 'login_id', 'process_name', 'time', 'user', 'user_sid'] |
| edit_regex_field | host |  | ['shost=({dest_host}({host}[^\s]+))'] |
| added_regex_field | dest_host |  | ['shost=({dest_host}({host}[^\s]+))'] |
| removed_attribute | DupFields |  | N/A |