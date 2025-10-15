# Code Changes for ibm-guardium-leef-database-activity-success-ibm (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['db_object', 'db_user', 'domain', 'host', 'process_name', 'service_name', 'sql_count', 'time', 'user'] |
| edit_regex_field | db_object |  | ['({process_name}[^\|]+)\|App\sUser\sName=({db_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))\|Service\sName=({service_name}[^\|]+)\|Object\/Field=({db_object}[^\|]+)\|Sum\sOf\sRecord\sAffected=({sql_count}\d+)'] |
| edit_regex_field | process_name |  | ['({process_name}[^\|]+)\|App\sUser\sName=({db_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))\|Service\sName=({service_name}[^\|]+)\|Object\/Field=({db_object}[^\|]+)\|Sum\sOf\sRecord\sAffected=({sql_count}\d+)'] |
| edit_regex_field | service_name |  | ['({process_name}[^\|]+)\|App\sUser\sName=({db_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))\|Service\sName=({service_name}[^\|]+)\|Object\/Field=({db_object}[^\|]+)\|Sum\sOf\sRecord\sAffected=({sql_count}\d+)'] |
| edit_regex_field | sql_count |  | ['({process_name}[^\|]+)\|App\sUser\sName=({db_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))\|Service\sName=({service_name}[^\|]+)\|Object\/Field=({db_object}[^\|]+)\|Sum\sOf\sRecord\sAffected=({sql_count}\d+)'] |
| edit_regex_field | user |  | ['({process_name}[^\|]+)\|App\sUser\sName=({db_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))\|Service\sName=({service_name}[^\|]+)\|Object\/Field=({db_object}[^\|]+)\|Sum\sOf\sRecord\sAffected=({sql_count}\d+)'] |
| added_regex_field | db_user |  | ['({process_name}[^\|]+)\|App\sUser\sName=({db_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))\|Service\sName=({service_name}[^\|]+)\|Object\/Field=({db_object}[^\|]+)\|Sum\sOf\sRecord\sAffected=({sql_count}\d+)'] |
| removed_attribute | DupFields |  | N/A |