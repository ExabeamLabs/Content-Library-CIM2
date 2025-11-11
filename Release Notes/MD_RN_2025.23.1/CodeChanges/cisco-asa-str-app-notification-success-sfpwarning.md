# Code Changes for cisco-asa-str-app-notification-success-sfpwarning (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | host |  | ['(\d+|({host}[\w\-\.]+))\s*:\s*(\d+\s)?\w+\s\d+\s\d\d:\d\d:\d\d', '\d+:\d+:\d+\s+({host}[\w\-.]+)\s*: \d\d\d\d'] |