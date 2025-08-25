# Code Changes for microsoft-mssql-kv-database-query-success-33205-2 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['db_domain', 'db_name', 'db_operation', 'db_query', 'db_user', 'dest_host', 'domain', 'event_code', 'host', 'result', 'schema_name', 'service_name', 'src_domain', 'src_ip', 'src_port', 'src_user', 'table_name', 'time', 'user', 'user_sid'] |
| edit_regex_field | db_user |  | ['\Wdatabase_principal_name:(({db_domain}[^\\\/:]+?)[\\\/]+)?({db_user}[^\s]+)(\s+\w+:|\s*$)'] |
| removed_regex_field | db_user_sid |  | [] |
| edit_regex_field | domain |  | ['\Wserver_principal_name:(({domain}[^\\\/:]+?)[\\\/]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)(\s+\w+:|\s*$)'] |
| edit_regex_field | user |  | ['\WUser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)(\s+\w+=|\s*$)', '\Wserver_principal_name:(({domain}[^\\\/:]+?)[\\\/]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)(\s+\w+:|\s*$)'] |
| edit_regex_field | user_sid |  | ['\WSid=({user_sid}[^\s]+?)(\s+\w+=|\s*$)', '\Wserver_principal_sid:({user_sid}[^\s]+)'] |
| added_regex_field | db_domain |  | ['\Wdatabase_principal_name:(({db_domain}[^\\\/:]+?)[\\\/]+)?({db_user}[^\s]+)(\s+\w+:|\s*$)'] |
| added_regex_field | src_domain |  | ['\Wsession_server_principal_name:(({src_domain}[^\\\/:]+?)[\\\/]+)?({src_user}[^\s]+)(\s+\w+:|\s*$)'] |
| added_regex_field | src_user |  | ['\Wsession_server_principal_name:(({src_domain}[^\\\/:]+?)[\\\/]+)?({src_user}[^\s]+)(\s+\w+:|\s*$)'] |