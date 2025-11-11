# Code Changes for microsoft-evadfs-kv-endpoint-login-success-1149 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'domain', 'event_code', 'host', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | host |  | ['ComputerName(:|=)\s*({dest_host}({host}[\w.-]+))'] |
| added_regex_field | dest_host |  | ['ComputerName(:|=)\s*({dest_host}({host}[\w.-]+))'] |
| removed_attribute | DupFields |  | N/A |