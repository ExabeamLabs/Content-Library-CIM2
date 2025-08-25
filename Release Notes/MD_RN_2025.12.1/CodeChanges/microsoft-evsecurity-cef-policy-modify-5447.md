# Code Changes for microsoft-evsecurity-cef-policy-modify-5447 (Parser)

| Code Change | Field Name | 2025.11.1 | 2025.12.1 |
|-------------|------------|-----------|------------|
| COULD_NOT_COMPARE | TimeFormat | yyyy-MM-dd'T'HH:mm:ss.SSS | ["yyyy-MM-dd'T'HH:mm:ss.SSS", 'MM/dd/yyyy hh:mm:ss a'] |
| changed | Conditions | ['5447', 'A Windows Filtering Platform filter has been changed', 'Change Information:', 'Microsoft-Windows-Security-Auditing'] | ['5447', 'A Windows Filtering Platform filter has been changed'] |
| edit_regex_field | time | ['({time}\d+-\d+-\d+T\d+:\d+:\d+\.\d+)', '({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)'] | ['({time}\d+-\d+-\d+T\d+:\d+:\d+\.\d+)', '({time}\d+\/\d+\/\d\d\d\d \d+:\d+:\d+ (?:(?i)am|pm))', '({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)'] |