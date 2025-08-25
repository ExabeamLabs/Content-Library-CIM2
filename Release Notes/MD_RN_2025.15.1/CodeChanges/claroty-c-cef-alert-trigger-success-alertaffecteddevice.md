# Code Changes for claroty-c-cef-alert-trigger-success-alertaffecteddevice (Parser)

| Code Change | Field Name | 2025.14.1 | 2025.15.1 |
|-------------|------------|-----------|------------|
| changed | Conditions | ['CEF:0|Claroty|Claroty|', '|alert_affected_device|'] | ['CEF:0|Claroty|', '|alert_affected_device|'] |
| edit_regex_field | time | ['\salert_timestamp=({time}[^\s]*)'] | ['\s({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\d\d\d\d)', '\salert_timestamp=({time}[^\s]*)'] |