# Code Changes for postgresql-p-csv-database-login-success-authentication (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | action |  | ['({action}connection authorized)', ':LOG:\s*({action}[^:]+)'] |
| edit_regex_field | additional_info |  | ['({additional_info}(connection authorized).+?)\s*$'] |
| edit_regex_field | app |  | ['application_name=({app}[^\s]+)'] |
| edit_regex_field | db_name |  | ['\sdatabase=({db_name}[^"\s=]+)', 'database=({db_name}[\w\.\-]+)'] |
| edit_regex_field | db_user |  | ['\s*user=({db_user}[^=]+?)\s'] |
| edit_regex_field | src_ip |  | ['connection authorized:\s*(\[[^\]]+\]:|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)?'] |
| edit_regex_field | src_port |  | ['connection authorized:\s*(\[[^\]]+\]:|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)?'] |