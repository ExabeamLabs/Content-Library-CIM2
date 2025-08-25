# Code Changes for microsoft-evsecurity-json-group-modify-success-4755 (Parser)

| Code Change | Field Name | 2025.14.1 | 2025.15.1 |
|-------------|------------|-----------|------------|
| edit_regex_field | host | ['"Hostname":"({host}[\w.-]+?)"'] | ['"Computer":"({host}[\w.-]+?)"', '"Hostname":"({host}[\w.-]+?)"'] |