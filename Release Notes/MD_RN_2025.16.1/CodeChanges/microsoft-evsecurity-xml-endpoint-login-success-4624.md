# Code Changes for microsoft-evsecurity-xml-endpoint-login-success-4624 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'auth_package', 'auth_process', 'dest_host', 'domain', 'email_address', 'event_code', 'event_id', 'event_name', 'host', 'key_length', 'login_id', 'login_type', 'process_dir', 'process_id', 'process_name', 'process_path', 'provider_name', 'result', 'result_code', 'run_level', 'src_host', 'src_host_windows', 'src_ip', 'src_port', 'subject_sid', 'time', 'user', 'user_sid'] |
| edit_regex_field | src_host_windows |  | ['<Data Name\\*=(\'|")WorkstationName(\'|")>([A-Fa-f:\d.]+|-|({src_host}({src_host_windows}[^<]+?)))\s*<'] |
| added_regex_field | src_host |  | ['<Data Name\\*=(\'|")WorkstationName(\'|")>([A-Fa-f:\d.]+|-|({src_host}({src_host_windows}[^<]+?)))\s*<'] |