# Code Changes for microsoft-evsecurity-json-user-password-reset-success-resetaccountspassword (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'dest_ip', 'dest_port', 'dest_user', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'src_ip', 'src_port', 'time', 'user', 'user_sid'] |
| edit_regex_field | host |  | ['"HostID":"({dest_host}({host}[\w\-.]+))'] |
| added_regex_field | dest_host |  | ['"HostID":"({dest_host}({host}[\w\-.]+))'] |
| removed_attribute | DupFields |  | N/A |