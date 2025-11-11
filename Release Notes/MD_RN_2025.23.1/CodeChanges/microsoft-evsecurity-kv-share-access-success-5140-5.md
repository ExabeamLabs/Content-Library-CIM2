# Code Changes for microsoft-evsecurity-kv-share-access-success-5140-5 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'd_name', 'd_parent', 'dest_host', 'domain', 'event_code', 'event_name', 'file_type', 'host', 'login_id', 'share_name', 'share_path', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | host |  | ['ComputerName=({dest_host}({host}[^\s]+))'] |
| added_regex_field | dest_host |  | ['ComputerName=({dest_host}({host}[^\s]+))'] |
| removed_attribute | DupFields |  | N/A |