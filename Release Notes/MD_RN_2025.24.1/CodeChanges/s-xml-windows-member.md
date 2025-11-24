# Code Changes for s-xml-windows-member (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'channel', 'dest_user_sid', 'event_code', 'event_id', 'event_name', 'group_domain', 'group_id', 'group_name', 'login_id', 'member', 'opcode', 'process_guid', 'process_id', 'provider_name', 'result', 'run_level', 'task_name', 'time', 'user_dn', 'user_ou', 'user_sid'] |
| removed_regex_field | account_domain |  | [] |
| removed_regex_field | account_name |  | [] |
| edit_regex_field | dest_user_sid |  | ['<Data Name(\\)?=(\'|")MemberSid(\'|")>({dest_user_sid}S-[^\s]+)<\/Data>'] |
| removed_regex_field | domain |  | [] |
| removed_regex_field | src_domain |  | [] |