# Code Changes for cisco-c-mix-ssh-traffic-success-loginsuccess (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | host |  | ['<\d+>[^:\s]+:\s+({host}[^:\s]+):', '\s\d\d:\d\d:\d\d\s({host}[^\s]+)\s\d+:', 'dvc=({host}[^\s]+)'] |