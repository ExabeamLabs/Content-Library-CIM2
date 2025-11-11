# Code Changes for microsoft-evsecurity-kv-endpoint-login-success-mcafee (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'login_type', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | host |  | ['shost=({dest_host}({host}[^\s]+))'] |
| added_regex_field | dest_host |  | ['shost=({dest_host}({host}[^\s]+))'] |
| removed_attribute | DupFields |  | N/A |