# Code Changes for defender-atp-security-alert-events (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | host |  | ['"hostname":"({host}[^"]+)"', 'exa_regex="hostName":"({host}[\w\-.]+)'] |