# Code Changes for unix-unix-str-file-write-success-audit (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | dest_host |  | ['\s({dest_host}({host}[\w\-.]+))\s*(vcsa-audit|audispd:|\w+:) '] |
| edit_regex_field | host |  | ['\s({dest_host}({host}[\w\-.]+))\s*(vcsa-audit|audispd:|\w+:) '] |