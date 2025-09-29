# Code Changes for microsoft-mcas-json-alert-trigger-success-ransomware (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | host |  | ['"hostname":"({host}[^"]+)"', 'exa_regex="hostName":"({host}[\w\-.]+)'] |