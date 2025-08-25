# Code Changes for citrix-cgateway-str-network-close-tcpconn (Parser)

| Code Change | Field Name | 2025.13.1 | 2025.14.1 |
|-------------|------------|-----------|------------|
| COULD_NOT_COMPARE | TimeFormat | MM/dd/yyyy:HH:mm:ss z | ['MM/dd/yyyy:HH:mm:ss z', "yyyy-MM-dd'T'HH:mm:ss"] |
| edit_regex_field | event_name | ['-PPE-\d+\s+:(\s+\w+)?\s+({event_name}TCP\s.+?)\s+\d+\s'] | ['({event_name}CONN_\w+)', '-PPE-\d+\s+:(\s+\w+)?\s+({event_name}TCP\s.+?)\s+\d+\s'] |
| edit_regex_field | time | ['Delink Time\s+({time}\d\d\/\d\d\/\d\d\d\d:\d\d:\d\d:\d\d \w+)', 'End Time\s+({time}\d\d\/\d\d\/\d\d\d\d:\d\d:\d\d:\d\d \w+)', '\s+({time}\d\d\/\d\d\/\d\d\d\d:\d\d:\d\d:\d\d \w+)\s+\S+\s+\d+-PPE-\d+\s*:'] | ['Delink Time\s+({time}\d\d\/\d\d\/\d\d\d\d:\d\d:\d\d:\d\d \w+)', 'End Time\s+({time}\d\d\/\d\d\/\d\d\d\d:\d\d:\d\d:\d\d \w+)', '\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)', '\s+({time}\d\d\/\d\d\/\d\d\d\d:\d\d:\d\d:\d\d \w+)\s+\S+\s+\d+-PPE-\d+\s*:'] |