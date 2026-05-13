# Code Changes for epic-siem-cef-app-login-fail-failedlogin (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'client_id', 'dest_host', 'dest_ip', 'dest_port', 'failure_reason', 'host', 'operation', 'resource', 'result', 'role', 'src_host', 'user'] |
| removed_regex_field | additional_info |  | [] |
| edit_regex_field | failure_reason |  | ['LOGINERROR=({failure_reason}.+?)\s+(\w+=|$)', 'MYCAUTHRESULT=({failure_reason}.+?)\s+(\w+=|$)'] |
| edit_regex_field | resource |  | ['USERJOB=(|([^\^]+)?\^({resource}.+?))\s+(\w+=|$)'] |
| edit_regex_field | user |  | ['LOGINLDAPID=({user}[\w\.\-\!\#\^\~]{1,40}\$?)', 'PREVUSER=({user}[\w\.\-\!\#\^\~]{1,40}\$?)'] |
| added_regex_field | account |  | ['NEWUSER=({account}[^\s,]+)'] |
| added_regex_field | client_id |  | ['LOGINCLIENTID=({client_id}.+?)\s+(\w+=|$)'] |
| added_regex_field | result |  | ['MASKMODE=({result}.+?)\s+(\w+=|$)'] |
| added_regex_field | role |  | ['ROLE=({role}.+?)(\s+\w+=|\s*$)'] |