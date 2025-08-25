# Code Changes for microsoft-evsecurity-cef-ds-object-modify-success-5136 (Parser)

| Code Change | Field Name | 2025.13.1 | 2025.14.1 |
|-------------|------------|-----------|------------|
| changed_parsed_fields | N/A | ['dest_host', 'dest_ip', 'domain', 'ds_object_dn', 'event_code', 'event_name', 'host', 'object_type', 'result', 'time', 'user'] | ['attribute', 'attribute_value', 'dest_host', 'dest_ip', 'domain', 'ds_object_dn', 'event_code', 'event_name', 'host', 'object_type', 'result', 'time', 'user'] |
| added_regex_field | attribute | [] | ['AttributeLDAPDisplayName=({attribute}[^\s]+)'] |
| added_regex_field | attribute_value | [] | ['AttributeValue=<({attribute_value}[^>]+)'] |