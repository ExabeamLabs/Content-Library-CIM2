# Code Changes for imperva-securesphere-cef-database-logout-securespherelogout (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'app', 'category', 'db_name', 'db_schema', 'db_user', 'dest_ip', 'dest_port', 'domain', 'host', 'protocol', 'server_group', 'service_name', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | db_user |  | ['\Wduser=(|(({domain}[^\\]+)\\)?({account}({db_user}[^\\]+?)))(\s+\w+=|\s*$)'] |
| edit_regex_field | domain |  | ['\Wcs12=(({domain}[^\\\s]+)\\+)?({host}[\w\-.]+)', '\Wduser=(|(({domain}[^\\]+)\\)?({account}({db_user}[^\\]+?)))(\s+\w+=|\s*$)'] |
| added_regex_field | account |  | ['\Wduser=(|(({domain}[^\\]+)\\)?({account}({db_user}[^\\]+?)))(\s+\w+=|\s*$)'] |
| removed_attribute | DupFields |  | N/A |