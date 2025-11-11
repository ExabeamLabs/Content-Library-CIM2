# Code Changes for microsoft-evsecurity-kv-endpoint-user-success-4648 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'account_domain', 'account_login_guid', 'dest_domain', 'dest_host', 'dest_service_name', 'dest_user', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'process_dir', 'process_id', 'process_name', 'process_path', 'src_ip', 'src_port', 'time', 'user', 'user_login_guid', 'user_sid'] |
| edit_regex_field | dest_domain |  | ['Used(:|=);?\s*Account Name(:|=)\s*({account}({dest_user}[^\s;@]+?))(@({account_domain}({dest_domain}[^\s;]+?)))?[\s;]*Account Domain(:|=)', 'Used(:|=)[^"]+?Account Domain(:|=)\s*(|({account_domain}({dest_domain}[^=:]*?)))[\s;]*Logon GUID(:|=)'] |
| edit_regex_field | dest_user |  | ['Used(:|=);?\s*Account Name(:|=)\s*({account}({dest_user}[^\s;@]+?))(@({account_domain}({dest_domain}[^\s;]+?)))?[\s;]*Account Domain(:|=)'] |
| added_regex_field | account |  | ['Used(:|=);?\s*Account Name(:|=)\s*({account}({dest_user}[^\s;@]+?))(@({account_domain}({dest_domain}[^\s;]+?)))?[\s;]*Account Domain(:|=)'] |
| added_regex_field | account_domain |  | ['Used(:|=);?\s*Account Name(:|=)\s*({account}({dest_user}[^\s;@]+?))(@({account_domain}({dest_domain}[^\s;]+?)))?[\s;]*Account Domain(:|=)', 'Used(:|=)[^"]+?Account Domain(:|=)\s*(|({account_domain}({dest_domain}[^=:]*?)))[\s;]*Logon GUID(:|=)'] |
| removed_attribute | DupFields |  | N/A |