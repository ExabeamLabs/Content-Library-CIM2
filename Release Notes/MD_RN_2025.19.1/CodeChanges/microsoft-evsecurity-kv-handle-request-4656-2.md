# Code Changes for microsoft-evsecurity-kv-handle-request-4656-2 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | user |  | ['Account Name:(\s|\\[rnt])*(-|({user}LOCAL SERVICE|SYSTEM|Administrator|NETWORK SERVICE|[\w\.\-\!\#\^\~]{1,40}\$?))(\s|\\[rnt])*Account Domain:'] |