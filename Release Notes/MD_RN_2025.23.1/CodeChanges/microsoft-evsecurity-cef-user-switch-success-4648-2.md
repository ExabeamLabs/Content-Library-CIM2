# Code Changes for microsoft-evsecurity-cef-user-switch-success-4648-2 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'dest_host', 'dest_user', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'process_dir', 'process_name', 'process_path', 'src_ip', 'src_port', 'time', 'user', 'user_sid'] |
| edit_regex_field | dest_user |  | ['duser=({account}({dest_user}[\w\-\.]+(?:\w+)?\$?))\s+suser'] |
| added_regex_field | account |  | ['duser=({account}({dest_user}[\w\-\.]+(?:\w+)?\$?))\s+suser'] |
| removed_attribute | DupFields |  | N/A |