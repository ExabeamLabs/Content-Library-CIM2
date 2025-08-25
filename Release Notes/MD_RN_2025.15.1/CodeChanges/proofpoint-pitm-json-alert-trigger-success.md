# Code Changes for proofpoint-pitm-json-alert-trigger-success (Parser)

| Code Change | Field Name | 2025.14.1 | 2025.15.1 |
|-------------|------------|-----------|------------|
| edit_regex_field | impact | ['exa_json_path=$..incident.severity,exa_regex=.+?severity:\d+:((?i)none|null|({impact}[^"]+))'] | ['exa_json_path=$..incident.severity,exa_regex=severity:\d+:((?i)none|null|({impact}[^"]+))'] |