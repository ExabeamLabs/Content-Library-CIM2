# Code Changes for unix-unix-str-app-notification-success-nomad (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| added_parser | N/A |  | {"Name": "unix-unix-str-app-notification-success-nomad", "Vendor": "Unix", "Product": "Unix", "TimeFormat": ["MMM dd HH:mm:ss"], "Conditions": ["nomad[", "]:"], "Fields": ["({time}\w\w\w \d\d \d\d:\d\d:\d\d)\s({host}[\w\-\.]+)\s({process_name}[^\[]+)\[({process_id}[^\]]+)]:.*?[^\d]:\s*({additional_info}[^$]+)"], "ParserVersion": "v1.0.0"} |