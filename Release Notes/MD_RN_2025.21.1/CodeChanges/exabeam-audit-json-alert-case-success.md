# Code Changes for exabeam-audit-json-alert-case-success (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_name', 'app', 'email_address', 'email_domain', 'method', 'new_value', 'object', 'object_id', 'object_name', 'old_value', 'operation', 'operation_type', 'result', 'rule', 'src_ip', 'time', 'url', 'user_info'] |
| edit_regex_field | object_name |  | ['"object_name":"({object}({object_name}.+?))",'] |
| added_regex_field | object |  | ['"object_name":"({object}({object_name}.+?))",'] |
| removed_attribute | DupFields |  | N/A |