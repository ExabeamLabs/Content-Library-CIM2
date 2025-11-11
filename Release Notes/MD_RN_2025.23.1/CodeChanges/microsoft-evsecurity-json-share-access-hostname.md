# Code Changes for microsoft-evsecurity-json-share-access-hostname (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'd_name', 'd_parent', 'dest_host', 'domain', 'event_code', 'event_name', 'file_dir', 'file_ext', 'file_name', 'file_type', 'host', 'login_id', 'result', 'share_name', 'share_path', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | host |  | ['\"Hostname\":\"({dest_host}({host}[^\"]+))'] |
| added_regex_field | dest_host |  | ['\"Hostname\":\"({dest_host}({host}[^\"]+))'] |
| removed_attribute | DupFields |  | N/A |