# Code Changes for unix-unix-str-endpoint-authentication-sshdaccepted (Parser)

| Code Change | Field Name | 2025.13.1 | 2025.14.1 |
|-------------|------------|-----------|------------|
| edit_attribute | TimeFormat | yyyy-MM-dd HH:mm:ss | yyyy-MM-dd'T'HH:mm:ss |
| changed_parsed_fields | N/A | ['additional_info', 'host'] | ['additional_info', 'host', 'time'] |
| added_regex_field | time | [] | ['({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)'] |