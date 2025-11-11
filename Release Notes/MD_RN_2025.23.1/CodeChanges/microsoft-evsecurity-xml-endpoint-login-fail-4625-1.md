# Code Changes for microsoft-evsecurity-xml-endpoint-login-fail-4625-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['auth_package', 'auth_process', 'dest_host', 'domain', 'event_code', 'event_name', 'failure_code', 'host', 'login_type', 'result_code', 'run_level', 'src_host', 'src_host_windows', 'src_ip', 'src_port', 'src_user', 'time', 'user', 'user_sid', 'user_upn'] |
| edit_regex_field | host |  | ['Computer>({dest_host}({host}[\w\-.]+))<\/Computer'] |
| edit_regex_field | src_host_windows |  | ['Workstation Name(:|=)\s*(-|({src_host_windows}({src_host}[\w\-\.]+)))[\s;]*Source Network Address(:|=)'] |
| added_regex_field | dest_host |  | ['Computer>({dest_host}({host}[\w\-.]+))<\/Computer'] |
| added_regex_field | src_host |  | ['Workstation Name(:|=)\s*(-|({src_host_windows}({src_host}[\w\-\.]+)))[\s;]*Source Network Address(:|=)'] |
| removed_attribute | DupFields |  | N/A |