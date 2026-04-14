# Code Changes for cisco-duo-sk4-app-activity-success-useradminupdate (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | app |  | ['"src-application-name":\s*"({app}[^"]+)"', 'destinationServiceName=({app}\S+)'] |
| edit_regex_field | event_name |  | ['"event-name":\s*"({event_name}[^"]+)"'] |
| edit_regex_field | first_name |  | ['"username":\s*"(({full_name}({first_name}[^\s"]+)\s({last_name}[^"]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"'] |
| edit_regex_field | full_name |  | ['"username":\s*"(({full_name}({first_name}[^\s"]+)\s({last_name}[^"]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"'] |
| edit_regex_field | last_name |  | ['"username":\s*"(({full_name}({first_name}[^\s"]+)\s({last_name}[^"]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"'] |
| edit_regex_field | object |  | ['"object":\s*"({object}[^"]+)"'] |
| edit_regex_field | operation |  | ['"action":\s*"({operation}[^"]+)"'] |
| edit_regex_field | user |  | ['"username":\s*"(({full_name}({first_name}[^\s"]+)\s({last_name}[^"]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"'] |