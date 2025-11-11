# Code Changes for microsoft-evsecurity-cef-user-delete-success-4726 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_name', 'aid', 'd_name', 'd_parent', 'dest_domain', 'dest_host', 'dest_ip', 'dest_port', 'dest_user', 'dest_user_sid', 'domain', 'event_code', 'event_name', 'full_name', 'host', 'login_id', 'result', 'share_name', 'share_path', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | dest_user |  | ['duser=({account_name}({dest_user}[^=]+))\s\w+='] |
| added_regex_field | account_name |  | ['duser=({account_name}({dest_user}[^=]+))\s\w+='] |
| removed_attribute | DupFields |  | N/A |