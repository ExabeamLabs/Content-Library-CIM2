# Code Changes for microsoft-evsecurity-xml-certificate-request-success-4886 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | attributes |  | ['<Data Name\\*=(\'|")Attributes(\'|")>\s*({attributes}[^<]+?)\s*<'] |
| edit_regex_field | domain |  | ['<Data Name\\*=(\'|")Requester(\'|")>(({domain}[^<\\]+)\\)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)<'] |
| edit_regex_field | process_id |  | ['<Execution ProcessID\\*=(\'|")({process_id}\d+)(\'|") ThreadID\\*=(\'|")({thread_id}\d+)(\'|")\/>'] |
| edit_regex_field | thread_id |  | ['<Execution ProcessID\\*=(\'|")({process_id}\d+)(\'|") ThreadID\\*=(\'|")({thread_id}\d+)(\'|")\/>'] |
| edit_regex_field | user |  | ['<Data Name\\*=(\'|")Requester(\'|")>(({domain}[^<\\]+)\\)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)<'] |