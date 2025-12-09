# Code Changes for github-g-json-branch-create-success-pullrequestcreate (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['app', 'company', 'domain', 'email_address', 'key_name', 'object', 'operation', 'operation_type', 'protocol', 'repository_name', 'src_ip', 'src_port', 'time', 'user', 'user_agent'] |
| edit_regex_field | object |  | ['"repo":\s*"({repository_name}({object}[^"]+))'] |
| added_regex_field | repository_name |  | ['"repo":\s*"({repository_name}({object}[^"]+))'] |
| removed_attribute | DupFields |  | N/A |