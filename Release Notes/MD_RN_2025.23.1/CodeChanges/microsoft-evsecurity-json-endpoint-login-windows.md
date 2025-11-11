# Code Changes for microsoft-evsecurity-json-endpoint-login-windows (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'dest_user', 'domain', 'event_name', 'failure_code', 'host', 'login_type_text', 'result_code', 'src_host', 'src_ip', 'user'] |
| edit_regex_field | host |  | ["exa_json_path=$.['data.system_name'],exa_regex=^({dest_host}({host}[\w\-.]+))$"] |
| edit_regex_field | result_code |  | ['exa_json_path=$.full_log,exa_regex=Error Code:\s*({failure_code}({result_code}[\w\-]+))'] |
| added_regex_field | dest_host |  | ["exa_json_path=$.['data.system_name'],exa_regex=^({dest_host}({host}[\w\-.]+))$"] |
| added_regex_field | failure_code |  | ['exa_json_path=$.full_log,exa_regex=Error Code:\s*({failure_code}({result_code}[\w\-]+))'] |
| removed_attribute | DupFields |  | N/A |