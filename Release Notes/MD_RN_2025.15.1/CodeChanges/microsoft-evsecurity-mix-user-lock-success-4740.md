# Code Changes for microsoft-evsecurity-mix-user-lock-success-4740 (Parser)

| Code Change | Field Name | 2025.14.1 | 2025.15.1 |
|-------------|------------|-----------|------------|
| edit_regex_field | event_name | ['({event_name}A user account was locked out)'] | ['({event_name}A user account was locked out)', 'exa_regex=({event_name}A user account was locked out)'] |