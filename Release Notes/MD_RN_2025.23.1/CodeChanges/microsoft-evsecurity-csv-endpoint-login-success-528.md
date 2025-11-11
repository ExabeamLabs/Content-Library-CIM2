# Code Changes for microsoft-evsecurity-csv-endpoint-login-success-528 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['auth_package', 'auth_process', 'dest_host', 'domain', 'event_code', 'event_id', 'event_name', 'host', 'login_id', 'login_type', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | host |  | ['(?:Success|Audit)\s+\w+\s+({dest_host}({host}[^\s]+))', 'Information\s+({dest_host}({host}[\w.\-]+))\s+'] |
| added_regex_field | dest_host |  | ['(?:Success|Audit)\s+\w+\s+({dest_host}({host}[^\s]+))', 'Information\s+({dest_host}({host}[\w.\-]+))\s+'] |
| removed_attribute | DupFields |  | N/A |