# Code Changes for microsoft-evsecurity-mix-share-access-success-5140-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | user |  | ['Account Name:\s*((\\)*(\\r|\\t|\\n))*(-|({user}LOCAL SERVICE|SYSTEM|Administrator|NETWORK SERVICE|[\w\.\-\!\#\^\~]{1,40}\$?))((\\)*(\\r|\\t|\\n))*\s*Account Domain:'] |