# Code Changes for microsoft-evsecurity-str-user-privilege-assign-success-4672 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| COULD_NOT_COMPARE | TimeFormat |  | ['yyyy-MM-dd HH:mm:ss', 'MMM dd HH:mm:ss'] |
| edit_regex_field | event_code |  | ['({event_code}4672)'] |
| edit_regex_field | host |  | ['({host}[\w.\-]+)[,\]]\s*新しいログオンに特権が割り当てられました。'] |
| edit_regex_field | time |  | ['({time}\d\d\d\d-\d\d-\d\d\s+\d\d:\d\d:\d\d),', '({time}\w{3}\s\d\d\s\d\d:\d\d:\d\d)'] |