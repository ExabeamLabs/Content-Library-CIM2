# Code Changes for microsoft-evsecurity-xml-ds-object-modify-success-5136 (Parser)

| Code Change | Field Name | 2025.13.1 | 2025.14.1 |
|-------------|------------|-----------|------------|
| changed_parsed_fields | N/A | ['attribute', 'dest_host', 'domain', 'ds_name', 'ds_object_dn', 'ds_type', 'event_code', 'event_name', 'host', 'login_id', 'object_type', 'run_level', 'time', 'user'] | ['attribute', 'attribute_value', 'dest_host', 'domain', 'ds_name', 'ds_object_dn', 'ds_type', 'event_code', 'event_name', 'host', 'login_id', 'object_type', 'operation_type', 'run_level', 'time', 'user'] |
| added_regex_field | attribute_value | [] | ['AttributeValue("|\')>({attribute_value}[^"\'<]+)</Data>'] |
| added_regex_field | operation_type | [] | ['<Data Name(\\)?=(\'|")OperationType(\'|")>({operation_type}[^<]+)'] |