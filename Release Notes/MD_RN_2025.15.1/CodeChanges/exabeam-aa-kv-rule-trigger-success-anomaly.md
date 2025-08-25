# Code Changes for exabeam-aa-kv-rule-trigger-success-anomaly (Parser)

| Code Change | Field Name | 2025.14.1 | 2025.15.1 |
|-------------|------------|-----------|------------|
| edit_regex_field | user | ['\suser="({user}[\w\.\-\!\#\^\~]{1,40}\$?)'] | ['\suser="({user}[^"]+)"'] |