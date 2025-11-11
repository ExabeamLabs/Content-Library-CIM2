# Code Changes for microsoft-evsecurity-kv-user-switch-success-4648 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'account_login_guid', 'dest_domain', 'dest_host', 'dest_service_name', 'dest_user', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'process_dir', 'process_id', 'process_name', 'process_path', 'src_ip', 'src_port', 'time', 'user', 'user_login_guid', 'user_sid'] |
| edit_regex_field | user |  | ['Subject(:|=).+?Account Name(:|=)\s*(?:-|SYSTEM|({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))[\s;]*Account Domain(:|=)'] |
| added_regex_field | account |  | ['Subject(:|=).+?Account Name(:|=)\s*(?:-|SYSTEM|({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))[\s;]*Account Domain(:|=)'] |
| removed_attribute | DupFields |  | N/A |