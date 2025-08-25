# Code Changes for microsoft-mssql-xml-database-login-success-33205 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | db_user |  | ['\Wserver_principal_name:(({domain}[^\\\/:]+?)[\\\/])?({db_user}[^\\\/\s]+?)(\s+\w+:|\s*$)'] |
| edit_regex_field | domain |  | ['\Wserver_principal_name:(({domain}[^\\\/:]+?)[\\\/])?({db_user}[^\\\/\s]+?)(\s+\w+:|\s*$)', '\\nserver_principal_name:((NT SERVICE|NT AUTHORITY|NT Service|({domain}[^\\]+))?\\+)?((?i)system|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\\nserver_principal_sid:'] |
| edit_regex_field | user |  | ['\WUser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)(\s+\w+=|\s*$)', '\\nserver_principal_name:((NT SERVICE|NT AUTHORITY|NT Service|({domain}[^\\]+))?\\+)?((?i)system|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\\nserver_principal_sid:'] |