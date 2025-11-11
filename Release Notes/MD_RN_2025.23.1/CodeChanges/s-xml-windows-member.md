# Code Changes for s-xml-windows-member (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_domain', 'account_name', 'additional_info', 'channel', 'dest_user_sid', 'domain', 'event_code', 'event_id', 'event_name', 'group_domain', 'group_id', 'group_name', 'login_id', 'member', 'opcode', 'process_guid', 'process_id', 'provider_name', 'result', 'run_level', 'src_domain', 'task_name', 'time', 'user_dn', 'user_ou', 'user_sid'] |
| removed_regex_field | dest_ip |  | [] |
| removed_regex_field | dest_port |  | [] |
| edit_regex_field | domain |  | ['<Data Name(\\)?=(\'|")SubjectDomainName(\'|")>({src_domain}({domain}[^<]+))</Data>'] |
| removed_regex_field | src_ip |  | [] |
| removed_regex_field | src_port |  | [] |
| removed_regex_field | user |  | [] |
| added_regex_field | src_domain |  | ['<Data Name(\\)?=(\'|")SubjectDomainName(\'|")>({src_domain}({domain}[^<]+))</Data>'] |
| removed_attribute | DupFields |  | N/A |