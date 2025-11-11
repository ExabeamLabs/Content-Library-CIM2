# Code Changes for microsoft-evsecurity-kv-user-password-reset-success-628 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_domain', 'dest_host', 'dest_user', 'dest_user_sid', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'time', 'user'] |
| edit_regex_field | host |  | ['Computer=({dest_host}({host}[^\s]+))'] |
| added_regex_field | dest_host |  | ['Computer=({dest_host}({host}[^\s]+))'] |
| removed_attribute | DupFields |  | N/A |