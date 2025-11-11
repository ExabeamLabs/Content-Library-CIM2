# Code Changes for microsoft-evsecurity-kv-share-access-success-5144 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'result', 'share_name', 'share_path', 'src_port', 'time', 'user', 'user_sid'] |
| edit_regex_field | host |  | ['ComputerName=({dest_host}({host}[^\s]+))'] |
| added_regex_field | dest_host |  | ['ComputerName=({dest_host}({host}[^\s]+))'] |
| removed_attribute | DupFields |  | N/A |