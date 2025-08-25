# Code Changes for microsoft-evsecurity-sk4-ds-object-modify-success-5136 (Parser)

| Code Change | Field Name | 2025.13.1 | 2025.14.1 |
|-------------|------------|-----------|------------|
| changed_parsed_fields | N/A | ['action', 'activity_id', 'app', 'dest_domain', 'dest_login_id', 'dest_user', 'dest_user_sid', 'domain', 'ds_object_dn', 'event_code', 'event_id', 'event_name', 'host', 'login_id', 'login_type', 'object_type', 'os', 'privileges', 'process_id', 'provider_name', 'result', 'sid_history', 'src_host', 'src_user', 'task_name', 'thread_id', 'time', 'user', 'user_sid'] | ['action', 'activity_id', 'app', 'attribute', 'attribute_value', 'dest_domain', 'dest_login_id', 'dest_user', 'dest_user_sid', 'domain', 'ds_object_dn', 'event_code', 'event_id', 'event_name', 'host', 'login_id', 'login_type', 'object_type', 'operation_type', 'os', 'privileges', 'process_id', 'provider_name', 'result', 'sid_history', 'src_host', 'src_user', 'task_name', 'thread_id', 'time', 'user', 'user_sid'] |
| added_regex_field | attribute | [] | ['AttributeLDAPDisplayName(\\)?":(\\)?"({attribute}[^"\\]+)'] |
| added_regex_field | attribute_value | [] | ['AttributeValue(\\)?":(\\)?"({attribute_value}[^"\'>\\]+)'] |
| added_regex_field | operation_type | [] | ['OperationType(\\)?":(\\)?"({operation_type}[^"\\]+)'] |