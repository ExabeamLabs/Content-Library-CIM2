# Code Changes for github-g-json-app-authentication-fail-accessrevoked (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'app', 'auth_type', 'company', 'domain', 'email_address', 'key_name', 'object', 'operation', 'operation_type', 'protocol', 'repository_name', 'src_ip', 'src_port', 'time', 'user', 'user_agent'] |
| edit_regex_field | object |  | ['"repo":\s*"({repository_name}({object}[^"]+))'] |
| added_regex_field | action |  | ['"action":\s*"({auth_type}({action}[^"]+))'] |
| added_regex_field | auth_type |  | ['"action":\s*"({auth_type}({action}[^"]+))'] |
| added_regex_field | repository_name |  | ['"repo":\s*"({repository_name}({object}[^"]+))'] |
| removed_attribute | DupFields |  | N/A |