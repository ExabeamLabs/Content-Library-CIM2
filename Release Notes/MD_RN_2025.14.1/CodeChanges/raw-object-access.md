# Code Changes for raw-object-access (ParserTemplate)

| Code Change | Field Name | 2025.13.1 | 2025.14.1 |
|-------------|------------|-----------|------------|
| edit_regex_field | time | ['({time}\w+\s+\d+\s+\d+:\d+:\d+\s+\d+)\s+({event_code}\d+)', 'EventTime":\s*"({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)"', '\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\.\d\d\d\d\d\d)?[+-]\d\d:\d\d)\s+'] | ['({time}\w+\s+\d+\s+\d+:\d+:\d+\s+\d+)\s+({event_code}\d+)', '<TimeCreated SystemTime(\\)?=(\'|")({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)', 'EventTime":\s*"({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)"', '\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\.\d\d\d\d\d\d)?[+-]\d\d:\d\d)\s+'] |