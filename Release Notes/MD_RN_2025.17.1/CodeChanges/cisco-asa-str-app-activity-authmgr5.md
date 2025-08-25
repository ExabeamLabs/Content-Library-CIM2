# Code Changes for cisco-asa-str-app-activity-authmgr5 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | host |  | ['(\d+|({host}[\w\-\.]+))\s*:\s*(\d+\s)?\w+\s\d+\s\d\d:\d\d:\d\d', '^[^:]+:\s(0.0.0.0|({host}[\w\.\-]+)):'] |