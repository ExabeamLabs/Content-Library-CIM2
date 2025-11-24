# Code Changes for microsoft-evsecurity-xml-group-member-remove-success-securitydisabled (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'channel', 'dest_ip', 'dest_port', 'dest_user_sid', 'domain', 'event_code', 'event_id', 'event_name', 'group_domain', 'group_id', 'group_name', 'host', 'login_id', 'member', 'opcode', 'process_guid', 'process_id', 'provider_name', 'result', 'run_level', 'src_domain', 'src_ip', 'src_port', 'src_user', 'task_name', 'time', 'user', 'user_dn', 'user_ou', 'user_sid'] |
| removed_regex_field | account_domain |  | [] |
| removed_regex_field | account_name |  | [] |
| edit_regex_field | dest_user_sid |  | ['<Data Name(\\)?=(\'|")MemberSid(\'|")>({dest_user_sid}S-[^\s]+)<\/Data>'] |