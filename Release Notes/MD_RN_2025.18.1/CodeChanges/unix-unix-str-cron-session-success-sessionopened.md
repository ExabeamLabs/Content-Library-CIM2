# Code Changes for unix-unix-str-cron-session-success-sessionopened (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| added_parser | N/A |  | {"Vendor": "Unix", "Product": "Unix", "TimeFormat": ["yyyy-MM-dd HH:mm:ss", "MMM dd HH:mm:ss"], "Fields": ["({time}\w+\s+\d+\s+\d+:\d+:\d+)\s*({host}[\w.\-]+)\s", "({event_name}session opened)\sfor user\s(root|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\sby"], "DupFields": ["host->dest_host"], "Name": "unix-unix-str-cron-session-success-sessionopened", "Conditions": ["pam_unix(cron:session)", "CRON[", " session opened "], "ParserVersion": "v1.0.0"} |