# Code Changes for trendmicro-ds-json-endpoint-login-fail-4625 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['auth_package', 'auth_process', 'domain', 'email_address', 'event_category', 'event_code', 'event_name', 'failure_code', 'failure_reason', 'host', 'login_id', 'login_type', 'os', 'result_code', 'src_domain', 'src_host', 'src_host_windows', 'src_ip', 'src_port', 'src_user', 'tenant_id', 'time', 'user', 'user_sid'] |
| edit_regex_field | result_code |  | ['Sub Status(:|=)\s*({failure_code}({result_code}[^\s;]+?))[\s;]*Process Information(:|=)'] |
| edit_regex_field | src_host |  | ['"Hostname\\*":\\*"(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({src_host}[\w\-\.]+))', 'Workstation Name(:|=)\s*(?:-|(::ffff:)?({src_host}({src_host_windows}[\w\-\.]+)))[\s;]*Source Network Address(:|=)'] |
| edit_regex_field | src_host_windows |  | ['Workstation Name(:|=)\s*(?:-|(::ffff:)?({src_host}({src_host_windows}[\w\-\.]+)))[\s;]*Source Network Address(:|=)'] |
| added_regex_field | failure_code |  | ['Sub Status(:|=)\s*({failure_code}({result_code}[^\s;]+?))[\s;]*Process Information(:|=)'] |
| removed_attribute | DupFields |  | N/A |