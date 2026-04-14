# Code Changes for squid-s-str-http-session-squidlog (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | mime |  | ['SQUID_LOG\s+(\S+\s*){9}(-|({mime}[^$\s]+))\s*'] |