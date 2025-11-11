# Code Changes for windows-events (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'auth_package', 'auth_process', 'event_code', 'event_name', 'failure_reason', 'file_dir', 'file_ext', 'file_name', 'file_path', 'login_id', 'login_type', 'object', 'object_class', 'operation_type', 'privileges', 'result', 'run_level', 'time', 'user_sid'] |
| removed_regex_field | domain |  | [] |
| edit_regex_field | login_id |  | ['(Primary)? Logon ID\s*:\s*\(?({login_id}.*?)\)?\s+Logon Type:'] |
| removed_regex_field | src_domain |  | [] |
| removed_regex_field | src_ip |  | [] |
| removed_regex_field | src_port |  | [] |
| removed_regex_field | src_user |  | [] |
| removed_regex_field | user |  | [] |