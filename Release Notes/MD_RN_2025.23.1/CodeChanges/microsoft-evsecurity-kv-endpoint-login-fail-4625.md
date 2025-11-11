# Code Changes for microsoft-evsecurity-kv-endpoint-login-fail-4625 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['auth_package', 'auth_process', 'dest_host', 'dest_ip', 'domain', 'event_code', 'event_name', 'failure_code', 'failure_reason', 'host', 'login_type', 'result', 'result_code', 'src_domain', 'src_host', 'src_host_windows', 'src_ip', 'src_port', 'src_user', 'time', 'user', 'user_sid', 'user_upn'] |
| edit_regex_field | result_code |  | ['Sub Status(:|=)\s*({failure_code}({result_code}[^\s;]+?))[\s;]*Process Information(:|=)'] |
| edit_regex_field | src_host_windows |  | ['Workstation Name(:|=)\s*(?:-|(::ffff:)?({src_host_windows}({src_host}[\w\-\.]+)))[\s;]*Source Network Address(:|=)'] |
| added_regex_field | failure_code |  | ['Sub Status(:|=)\s*({failure_code}({result_code}[^\s;]+?))[\s;]*Process Information(:|=)'] |
| added_regex_field | src_host |  | ['Workstation Name(:|=)\s*(?:-|(::ffff:)?({src_host_windows}({src_host}[\w\-\.]+)))[\s;]*Source Network Address(:|=)'] |
| removed_attribute | DupFields |  | N/A |