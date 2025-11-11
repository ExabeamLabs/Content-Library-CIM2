# Code Changes for microsoft-evadfs-kv-rdp-traffic-success-remoteconnect (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'domain', 'event_code', 'event_name', 'host', 'src_ip', 'src_port', 'time', 'user', 'user_upn'] |
| edit_regex_field | host |  | ['Information\s+({dest_host}({host}[^\s]+))'] |
| added_regex_field | dest_host |  | ['Information\s+({dest_host}({host}[^\s]+))'] |
| removed_attribute | DupFields |  | N/A |