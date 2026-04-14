# Code Changes for postfix-postfix-str-smtp-close-connectionfail (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | host |  | ['({time}\w\w\w \d\d \d\d:\d\d:\d\d)\s({host}[\w\-\.]+)\s({process_name}[^\[]+)\[({process_id}[^\]]+)]\s*({message_id}[\w]+)', '\s*(::ffff:)?({host}[^\s]+)?\s*postfix'] |