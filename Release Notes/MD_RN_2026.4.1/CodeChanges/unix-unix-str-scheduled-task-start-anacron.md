# Code Changes for unix-unix-str-scheduled-task-start-anacron (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | host |  | ['(::ffff:)?({host}\S+)\sCROND', '({time}(\w{3}\s*\d\d?\s\d\d:\d\d:\d\d)|(\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d+[+\-]\d\d:\d\d))\s(::ffff:)?({host}[\w\-.]+)\s', '\d\d:\d\d:\d\d\s((::ffff:)?({dest_ip}[A-Fa-f:\d.]*)\s+)?(::ffff:)?({host}[^\s]+)\s*({additional_info}run-parts.+?)\s*$'] |