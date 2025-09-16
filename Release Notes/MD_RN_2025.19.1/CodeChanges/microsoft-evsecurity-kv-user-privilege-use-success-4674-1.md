# Code Changes for microsoft-evsecurity-kv-user-privilege-use-success-4674-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | domain |  | ['Account Name:\s*(-|({user}LOCAL SERVICE|SYSTEM|Administrator|NETWORK SERVICE|[\w\.\-\!\#\^\~]{1,40}\$?))\s+Account Domain:\s*(-|NT AUTHORITY|({domain}[^":]+?))\s'] |
| edit_regex_field | user |  | ['Account Name:\s*(-|({user}LOCAL SERVICE|SYSTEM|Administrator|NETWORK SERVICE|[\w\.\-\!\#\^\~]{1,40}\$?))\s+Account Domain:\s*(-|NT AUTHORITY|({domain}[^":]+?))\s'] |