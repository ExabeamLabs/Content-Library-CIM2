# Code Changes for microsoft-evsecurity-kv-endpoint-login-fail-4625-3 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['auth_package', 'auth_process', 'dest_host', 'domain', 'event_code', 'event_name', 'failure_code', 'host', 'key_length', 'login_id', 'login_type', 'result_code', 'src_domain', 'src_host', 'src_host_windows', 'src_ip', 'src_port', 'src_user', 'time', 'user', 'user_sid'] |
| edit_regex_field | dest_host |  | [',(Audit Failure|Failure Audit|Information),({host}({dest_host}[\w\-.]+)),'] |
| edit_regex_field | result_code |  | ['\s*Sub Status:\s*({failure_code}({result_code}.+?))[\s;]*Process Information:'] |
| edit_regex_field | src_host_windows |  | ['Workstation Name:\s+({src_host_windows}({src_host}[\w\-\.]+))\s+Source Network'] |
| added_regex_field | failure_code |  | ['\s*Sub Status:\s*({failure_code}({result_code}.+?))[\s;]*Process Information:'] |
| added_regex_field | host |  | [',(Audit Failure|Failure Audit|Information),({host}({dest_host}[\w\-.]+)),'] |
| added_regex_field | src_host |  | ['Workstation Name:\s+({src_host_windows}({src_host}[\w\-\.]+))\s+Source Network'] |
| removed_attribute | DupFields |  | N/A |