# Code Changes for microsoft-evsecurity-json-peripheral-storage-insert-success-6416 (Parser)

| Code Change | Field Name | 2025.14.1 | 2025.15.1 |
|-------------|------------|-----------|------------|
| changed_parsed_fields | N/A | ['device_class', 'device_description', 'device_id', 'domain', 'login_id', 'user'] | ['device_class', 'device_description', 'device_id', 'domain', 'event_name', 'login_id', 'user'] |
| added_regex_field | event_name | [] | ['exa_regex=({event_name}A new external device was recognized by the system.)'] |