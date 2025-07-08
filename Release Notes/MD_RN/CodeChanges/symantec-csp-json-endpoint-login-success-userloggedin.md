# Code Changes for symantec-csp-json-endpoint-login-success-userloggedin (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A | ['dest_ip', 'dest_port', 'domain', 'event_code', 'event_name', 'host', 'login_type_text', 'parent_process_path', 'policy_name', 'process_name', 'result', 'rule', 'session_id', 'src_ip', 'src_port', 'time', 'user'] | ['dest_ip', 'dest_port', 'domain', 'event_code', 'event_name', 'host', 'login_type_text', 'parent_process_path', 'policy_name', 'process_dir', 'process_name', 'process_path', 'result', 'rule', 'session_id', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | process_name | ['\sPROCESS_PATH\s*:\s*"+({process_name}[^"\s]+)'] | ['\sPROCESS_PATH\s*:\s*"+({process_path}({process_dir}[^"]*[\\\/]+)?({process_name}[^":]+?))"'] |
| added_regex_field | process_dir | [] | ['\sPROCESS_PATH\s*:\s*"+({process_path}({process_dir}[^"]*[\\\/]+)?({process_name}[^":]+?))"'] |
| added_regex_field | process_path | [] | ['\sPROCESS_PATH\s*:\s*"+({process_path}({process_dir}[^"]*[\\\/]+)?({process_name}[^":]+?))"'] |