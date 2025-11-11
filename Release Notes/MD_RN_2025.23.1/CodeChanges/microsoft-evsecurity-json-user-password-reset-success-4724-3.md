# Code Changes for microsoft-evsecurity-json-user-password-reset-success-4724-3 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_domain', 'dest_host', 'dest_user', 'dest_user_sid', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'time', 'user', 'user_sid'] |
| edit_regex_field | host |  | ['"MachineName":"({dest_host}({host}[\w\-.]+))'] |
| added_regex_field | dest_host |  | ['"MachineName":"({dest_host}({host}[\w\-.]+))'] |
| removed_attribute | DupFields |  | N/A |