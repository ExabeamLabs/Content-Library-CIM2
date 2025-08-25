# Code Changes for cisco-asa-str-endpoint-login-fail-2960 (Parser)

| Code Change | Field Name | 2025.13.1 | 2025.14.1 |
|-------------|------------|-----------|------------|
| changed_parsed_fields | N/A | ['event_code', 'event_name', 'host', 'result', 'src_interface', 'src_mac', 'time'] | ['event_code', 'event_name', 'host', 'result', 'src_host', 'src_interface', 'src_mac', 'time'] |
| added_regex_field | src_host | [] | ['Username:\s*host\/({src_host}[\w\-]+)'] |