# Code Changes for unix-unix-str-endpoint-notification-success-cron (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| COULD_NOT_COMPARE | TimeFormat |  | ['yyyy-MM-dd HH:mm:ss', 'MMM dd HH:mm:ss'] |
| changed_parsed_fields | N/A |  | ['account', 'additional_info', 'host', 'process_command_line', 'time'] |
| edit_regex_field | host |  | ['({time}\w{3}\s+\d+\s+\d\d:\d\d:\d\d)\s+(::ffff:)?({host}[\w\-.]+)', '\d\d:\d\d:\d\d(\.\S+)? (::ffff:)?({host}\S+)? f?cron\['] |
| added_regex_field | account |  | ['\(({account}[^\)]+?)\) CMD'] |
| added_regex_field | process_command_line |  | ['\sCMD \(\s*({process_command_line}.+?)\)($|\s|")'] |
| added_regex_field | time |  | ['({time}\w{3}\s+\d+\s+\d\d:\d\d:\d\d)\s+(::ffff:)?({host}[\w\-.]+)'] |