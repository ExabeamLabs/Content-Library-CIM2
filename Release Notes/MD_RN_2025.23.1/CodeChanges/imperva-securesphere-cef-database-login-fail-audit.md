# Code Changes for imperva-securesphere-cef-database-login-fail-audit (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'app', 'db_name', 'db_schema', 'db_user', 'dest_ip', 'dest_port', 'domain', 'host', 'protocol', 'result_reason', 'server_group', 'service_name', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | db_user |  | ['\Wduser=(({domain}[^\\\s]+)\\+)?({account}({db_user}[^\s]+))'] |
| edit_regex_field | domain |  | ['\Wcs11="*(({domain}[^\\\s",]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)"*\s*(\w+=|$)', '\Wcs12=(({domain}[^\\\s]+)\\+)?({host}[\w\-.]+)', '\Wduser=(({domain}[^\\\s]+)\\+)?({account}({db_user}[^\s]+))'] |
| added_regex_field | account |  | ['\Wduser=(({domain}[^\\\s]+)\\+)?({account}({db_user}[^\s]+))'] |
| removed_attribute | DupFields |  | N/A |