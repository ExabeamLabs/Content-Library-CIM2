# Code Changes for microsoft-evsecurity-json-share-access-5145 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'd_name', 'd_parent', 'dest_host', 'domain', 'event_code', 'event_name', 'file_dir', 'file_ext', 'file_name', 'file_type', 'host', 'login_id', 'result', 'share_name', 'share_path', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | host |  | ['Computer(Name)?\s*\\*\"?(=|:|>)\s*\"*({dest_host}({host}[\w\.-]+))(\s|,|\"|</Computer>|$)'] |
| added_regex_field | dest_host |  | ['Computer(Name)?\s*\\*\"?(=|:|>)\s*\"*({dest_host}({host}[\w\.-]+))(\s|,|\"|</Computer>|$)'] |
| removed_attribute | DupFields |  | N/A |