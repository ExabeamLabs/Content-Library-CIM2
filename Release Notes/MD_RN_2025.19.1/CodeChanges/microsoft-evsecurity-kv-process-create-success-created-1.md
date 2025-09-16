# Code Changes for microsoft-evsecurity-kv-process-create-success-created-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | user |  | ["Creator Subject:.+?Account Name:(\\+[rnt]|\s)*'?(-|({user}LOCAL SERVICE|SYSTEM|Administrator|NETWORK SERVICE|[\w\.\-\!\#\^\~]{1,40}\$?))", 'Subject:.+?Account Name:\s*(-|SYSTEM|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*\w+\s\w+:'] |