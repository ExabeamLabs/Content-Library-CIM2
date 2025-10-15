# Code Changes for microsoft-evsecurity-kv-ds-object-delete-success-5141-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'attribute', 'domain', 'event_code', 'event_id', 'event_name', 'host', 'login_id', 'new_attribute', 'object_name', 'object_type', 'old_attribute', 'operation_type', 'src_host', 'src_ip', 'src_port', 'time', 'user', 'user_sid'] |
| edit_regex_field | operation_type |  | ['REMARKS\s*=\s*(null|-|({event_name}({operation_type}[^\]]+?)))\s*\]'] |
| added_regex_field | event_name |  | ['REMARKS\s*=\s*(null|-|({event_name}({operation_type}[^\]]+?)))\s*\]'] |
| removed_attribute | DupFields |  | N/A |