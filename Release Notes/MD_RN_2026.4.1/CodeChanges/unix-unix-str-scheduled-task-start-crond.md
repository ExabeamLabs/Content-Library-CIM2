# Code Changes for unix-unix-str-scheduled-task-start-crond (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | host |  | ['(::ffff:)?({host}\S+)\sCROND', '({time}\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2}(.\d+)?Z)\s(::ffff:)?({host}[\w\-.]+)\s', '({time}\w+\s+\d{2}\s+\d{2}:\d{2}:\d{2})\s*({host}[\w.\-]+)\s', '\d\d:\d\d:\d\d (::ffff:)?({host}\S+)? crond\['] |