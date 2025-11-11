# Code Changes for microsoft-evsecurity-json-endpoint-login-success-540 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['auth_process', 'dest_host', 'event_name', 'host', 'login_id', 'src_ip', 'src_port', 'user'] |
| edit_regex_field | host |  | ['exa_json_path=$.computer_name,exa_regex=^({dest_host}({host}[\w\-.]+?))$'] |
| added_regex_field | dest_host |  | ['exa_json_path=$.computer_name,exa_regex=^({dest_host}({host}[\w\-.]+?))$'] |
| removed_attribute | DupFields |  | N/A |