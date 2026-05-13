# Code Changes for epic-siem-cef-app-activity-success-maskeddatadisplay (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | full_name |  | ['suser=([^\^]+)?\^({full_name}[^\^]+)\^({user}[\w\.\-\!\#\^\~]{1,40}\$?)?'] |
| edit_regex_field | user |  | ['PREVUSER=({user}[\w\.\-\!\#\^\~]{1,40}\$?)', 'suser=([^\^]+)?\^({full_name}[^\^]+)\^({user}[\w\.\-\!\#\^\~]{1,40}\$?)?'] |