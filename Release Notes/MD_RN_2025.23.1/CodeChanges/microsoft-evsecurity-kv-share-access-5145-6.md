# Code Changes for microsoft-evsecurity-kv-share-access-5145-6 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'd_name', 'd_parent', 'dest_host', 'domain', 'event_code', 'event_name', 'file_dir', 'file_ext', 'file_name', 'file_type', 'host', 'login_id', 'result', 'share_name', 'share_path', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | host |  | ['({dest_host}({host}[\w\-.]+))\s+(?i)((audit|success)( |_)(success|audit))'] |
| added_regex_field | dest_host |  | ['({dest_host}({host}[\w\-.]+))\s+(?i)((audit|success)( |_)(success|audit))'] |
| removed_attribute | DupFields |  | N/A |