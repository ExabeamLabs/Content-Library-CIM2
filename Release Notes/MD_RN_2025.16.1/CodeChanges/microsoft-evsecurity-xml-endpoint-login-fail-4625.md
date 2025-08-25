# Code Changes for microsoft-evsecurity-xml-endpoint-login-fail-4625 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_name', 'auth_package', 'auth_process', 'dest_domain', 'dest_host', 'dest_user', 'domain', 'email_address', 'email_domain', 'event_code', 'event_name', 'failure_code', 'failure_reason', 'host', 'key_length', 'login_type', 'result_code', 'run_level', 'src_domain', 'src_host', 'src_host_windows', 'src_ip', 'src_port', 'src_user', 'subject_sid', 'time', 'user', 'user_sid'] |
| edit_regex_field | src_host_windows |  | ['<Data Name(\\)?=(\'|")WorkstationName(\'|")>(-|(?i)WORKSTATION|({src_host}({src_host_windows}[A-Za-z]+[\w.-]+)))\s*</Data>'] |
| added_regex_field | src_host |  | ['<Data Name(\\)?=(\'|")WorkstationName(\'|")>(-|(?i)WORKSTATION|({src_host}({src_host_windows}[A-Za-z]+[\w.-]+)))\s*</Data>'] |