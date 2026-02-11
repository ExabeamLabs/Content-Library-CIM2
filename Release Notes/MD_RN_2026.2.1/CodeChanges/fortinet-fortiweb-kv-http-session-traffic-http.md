# Code Changes for fortinet-fortiweb-kv-http-session-traffic-http (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | method |  | ['http_method="?({method}[^=]+?)"?\s\w+='] |