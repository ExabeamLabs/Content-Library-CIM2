# Code Changes for microsoft-evsecurity-kv-ds-object-modify-success-4742 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_name', 'additional_info', 'attribute', 'dest_host', 'domain', 'event_code', 'event_id', 'event_name', 'host', 'login_id', 'new_attribute', 'new_value', 'object', 'object_type', 'old_attribute', 'old_value', 'operation_type', 'src_host', 'src_ip', 'src_port', 'time', 'uac_status', 'user', 'user_sid'] |
| edit_regex_field | account_name |  | ['ACCOUNT_NAME\s*=\s*(null|-|({object}({account_name}[^\s]+)))'] |
| edit_regex_field | host |  | ['({dest_host}({host}[\w\-.]+)) ADAuditPlus'] |
| edit_regex_field | object_type |  | ["FORMAT_MESSAGE\s*=\s*(null|-|({additional_info}({object_type}[^\']+?)))\s*'"] |
| edit_regex_field | operation_type |  | ['REMARKS\s*=\s*(null|-|({event_name}({operation_type}[^\]]+?)))\s*\]'] |
| added_regex_field | additional_info |  | ["FORMAT_MESSAGE\s*=\s*(null|-|({additional_info}({object_type}[^\']+?)))\s*'"] |
| added_regex_field | dest_host |  | ['({dest_host}({host}[\w\-.]+)) ADAuditPlus'] |
| added_regex_field | event_name |  | ['REMARKS\s*=\s*(null|-|({event_name}({operation_type}[^\]]+?)))\s*\]'] |
| added_regex_field | object |  | ['ACCOUNT_NAME\s*=\s*(null|-|({object}({account_name}[^\s]+)))'] |
| removed_attribute | DupFields |  | N/A |