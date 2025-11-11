# Code Changes for windows-events-wls (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_id', 'account_name', 'auth_package', 'auth_process', 'client', 'dest_domain', 'dest_user', 'dest_user_sid', 'domain', 'event_code', 'failure_reason', 'key_length', 'login_id', 'login_type', 'object_server', 'process_command_line', 'process_dir', 'process_guid', 'process_id', 'process_name', 'process_path', 'result_code', 'service_name', 'service_type', 'src_domain', 'src_ip', 'src_port', 'time', 'user_dn', 'user_sid'] |
| edit_regex_field | domain |  | ['SubjectDomainName="+(-|({src_domain}({domain}[^"]+)))"'] |
| removed_regex_field | user |  | [] |
| added_regex_field | src_domain |  | ['SubjectDomainName="+(-|({src_domain}({domain}[^"]+)))"'] |