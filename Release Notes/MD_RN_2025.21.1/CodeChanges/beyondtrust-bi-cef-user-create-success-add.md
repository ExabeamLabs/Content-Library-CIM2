# Code Changes for beyondtrust-bi-cef-user-create-success-add (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_domain', 'account_name', 'app', 'dest_ip', 'dest_user', 'domain', 'host', 'operation', 'severity', 'src_host', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | account_domain |  | ['dhost=(({account_domain}[^\/,\s]+?)[\\\/]+)?({dest_user}({account_name}[^,\s]+))', 'dhost=(Asset:({src_host}[^\s]+)\sAccount:)(({account_domain}[\w\.\-]+?)[\\]+)?({dest_user}({account_name}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| edit_regex_field | account_name |  | ['dhost=(({account_domain}[^\/,\s]+?)[\\\/]+)?({dest_user}({account_name}[^,\s]+))', 'dhost=(Asset:({src_host}[^\s]+)\sAccount:)(({account_domain}[\w\.\-]+?)[\\]+)?({dest_user}({account_name}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| edit_regex_field | src_host |  | ['dhost=(Asset:({src_host}[^\s]+)\sAccount:)(({account_domain}[\w\.\-]+?)[\\]+)?({dest_user}({account_name}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| added_regex_field | dest_user |  | ['dhost=(({account_domain}[^\/,\s]+?)[\\\/]+)?({dest_user}({account_name}[^,\s]+))', 'dhost=(Asset:({src_host}[^\s]+)\sAccount:)(({account_domain}[\w\.\-]+?)[\\]+)?({dest_user}({account_name}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| removed_attribute | DupFields |  | N/A |