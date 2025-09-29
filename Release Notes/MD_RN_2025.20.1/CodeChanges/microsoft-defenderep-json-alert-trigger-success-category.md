# Code Changes for microsoft-defenderep-json-alert-trigger-success-category (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | host |  | ['"hostname":"({host}[^"]+)"', 'exa_regex="hostName":"({host}[\w\-.]+)'] |