# Code Changes for microsoft-evsecurity-kv-user-password-reset-success-4724-2 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_domain', 'dest_host', 'dest_user', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'src_ip', 'src_port', 'time', 'user', 'user_sid'] |
| edit_regex_field | host |  | ['shost=({dest_host}({host}[\w\-.]+))'] |
| added_regex_field | dest_host |  | ['shost=({dest_host}({host}[\w\-.]+))'] |
| removed_attribute | DupFields |  | N/A |