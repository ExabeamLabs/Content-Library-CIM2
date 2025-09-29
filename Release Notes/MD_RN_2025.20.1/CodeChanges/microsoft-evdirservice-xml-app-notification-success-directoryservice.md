# Code Changes for microsoft-evdirservice-xml-app-notification-success-directoryservice (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | domain |  | ['<EventData><Data>\d+\.\d+\.\d+\.\d+:\d+<\/Data><Data>(({domain}[^<]+)\\({user}[\w\.\-\!\#\^\~]{1,40}\$?))', 'Identity the client attempted to authenticate as:\s*(({domain}[^\\]+)\\)?({user}ANONYMOUS LOGON|[\w\.\-\!\#\^\~]{1,40}\$?)'] |
| edit_regex_field | user |  | ['<EventData><Data>\d+\.\d+\.\d+\.\d+:\d+<\/Data><Data>(({domain}[^<]+)\\({user}[\w\.\-\!\#\^\~]{1,40}\$?))', 'Identity the client attempted to authenticate as:\s*(({domain}[^\\]+)\\)?({user}ANONYMOUS LOGON|[\w\.\-\!\#\^\~]{1,40}\$?)'] |