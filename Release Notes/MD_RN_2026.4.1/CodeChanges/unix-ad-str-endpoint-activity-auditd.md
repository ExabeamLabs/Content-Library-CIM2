# Code Changes for unix-ad-str-endpoint-activity-auditd (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | host |  | ['\d\d:\d\d:\d\d (\d+|({host}[\w\-.]+)).+?auditd', '\s+\d+\s\d\d:\d\d:\d\d\s*\[({host}[\w\-.]+)\]:?\s*auditd\['] |