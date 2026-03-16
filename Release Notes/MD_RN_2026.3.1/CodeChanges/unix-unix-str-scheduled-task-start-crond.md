# Code Changes for unix-unix-str-scheduled-task-start-crond (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| COULD_NOT_COMPARE | TimeFormat |  | ["yyyy-MM-dd'T'HH:mm:ssZ", 'MMM dd HH:mm:ss', "yyyy-MM-dd'T'HH:mm:ss.SSSZ"] |
| edit_regex_field | host |  | ['({time}\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2}(.\d+)?Z)\s(::ffff:)?({host}[\w\-.]+)\s', '({time}\w+\s+\d{2}\s+\d{2}:\d{2}:\d{2})\s*({host}[\w.\-]+)\s', '\d\d:\d\d:\d\d (::ffff:)?({host}\S+)? crond\['] |
| edit_regex_field | time |  | ['({time}\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2}(.\d+)?Z)\s(::ffff:)?({host}[\w\-.]+)\s', '({time}\w+\s+\d{2}\s+\d{2}:\d{2}:\d{2})\s*({host}[\w.\-]+)\s'] |