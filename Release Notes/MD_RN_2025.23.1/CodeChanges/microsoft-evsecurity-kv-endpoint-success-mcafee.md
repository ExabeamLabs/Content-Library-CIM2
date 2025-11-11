# Code Changes for microsoft-evsecurity-kv-endpoint-success-mcafee (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['auth_package', 'dest_host', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'login_type', 'src_ip', 'src_port', 'time', 'user', 'user_sid'] |
| edit_regex_field | host |  | ['shost=({dest_host}({host}[\w\-.]+))'] |
| added_regex_field | dest_host |  | ['shost=({dest_host}({host}[\w\-.]+))'] |
| removed_attribute | DupFields |  | N/A |