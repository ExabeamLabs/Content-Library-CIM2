# Code Changes for microsoft-evapp-json-endpoint-activity-success-catchall (Parser)

| Code Change | Field Name | 2025.14.1 | 2025.15.1 |
|-------------|------------|-----------|------------|
| changed_parsed_fields | N/A | ['domain', 'event_name', 'user', 'user_sid'] | ['additional_info', 'domain', 'event_name', 'user', 'user_sid'] |
| added_regex_field | additional_info | [] | ['exa_json_path=$.StringInserts,exa_regex=(\[\]|.+?"({additional_info}[^"]+))'] |