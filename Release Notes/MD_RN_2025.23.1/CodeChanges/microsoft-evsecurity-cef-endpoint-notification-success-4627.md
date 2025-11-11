# Code Changes for microsoft-evsecurity-cef-endpoint-notification-success-4627 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'domain', 'event_code', 'event_name', 'group_membership', 'host', 'login_id', 'login_type', 'result', 'time', 'user'] |
| edit_regex_field | host |  | ['\sdvchost=({dest_host}({host}[^\s]+))'] |
| added_regex_field | dest_host |  | ['\sdvchost=({dest_host}({host}[^\s]+))'] |
| removed_attribute | DupFields |  | N/A |