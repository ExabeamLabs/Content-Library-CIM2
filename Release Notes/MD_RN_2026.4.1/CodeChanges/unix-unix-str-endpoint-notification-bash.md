# Code Changes for unix-unix-str-endpoint-notification-bash (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | host |  | ['({time}\w+\s*\d+ \d\d:\d\d:\d\d)\s*(\d+|({host}[^\s]+))\s*kernel:', '({time}\w+\s*\d+ \d\d:\d\d:\d\d)\s*({host}[^\s]+)\s*bash\['] |
| edit_regex_field | time |  | ['({time}\w+\s*\d+ \d\d:\d\d:\d\d)\s*(\d+|({host}[^\s]+))\s*kernel:', '({time}\w+\s*\d+ \d\d:\d\d:\d\d)\s*({host}[^\s]+)\s*bash\['] |