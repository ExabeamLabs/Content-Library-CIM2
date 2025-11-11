# Code Changes for microsoft-evsecurity-kv-share-access-success-5145 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'access_mask', 'access_reason', 'dest_host', 'domain', 'event_code', 'event_name', 'file_dir', 'file_ext', 'file_name', 'file_path', 'file_type', 'host', 'login_id', 'share_name', 'share_path', 'src_ip', 'src_port', 'user', 'user_sid'] |
| edit_regex_field | host |  | ['\d\d:\d\d:\d\d\s+({dest_host}({host}[\w\-.]+))\s+(CEF|dsa_lca):'] |
| added_regex_field | dest_host |  | ['\d\d:\d\d:\d\d\s+({dest_host}({host}[\w\-.]+))\s+(CEF|dsa_lca):'] |
| removed_attribute | DupFields |  | N/A |