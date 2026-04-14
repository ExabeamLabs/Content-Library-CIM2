# Code Changes for unix-unix-str-smtp-close-lostconnection (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | host |  | ['\d\d:\d\d:\d\d\s(::ffff:)?(({dest_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+))|({dest_host}[\w\-.]+))\s*(::ffff:)?({host}[^\s]+)?\s*postfix', '\s*(::ffff:)?({host}[^\s]+)?\s*postfix', '\w{3}\s\d\d\s\d\d:\d\d:\d\d\s(::ffff:)?({host}[\w\-.]+)\s'] |