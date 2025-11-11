# Code Changes for microsoft-evsecurity-kv-group-member-add-success-4756-2 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_domain', 'account_name', 'additional_info', 'dest_host', 'dest_ip', 'dest_port', 'dest_user_sid', 'domain', 'event_code', 'group_domain', 'group_id', 'group_name', 'host', 'login_id', 'member', 'process_guid', 'process_id', 'provider_name', 'run_level', 'src_domain', 'src_ip', 'src_port', 'src_user', 'thread_id', 'time', 'user', 'user_dn', 'user_ou', 'user_sid'] |
| edit_regex_field | domain |  | ['<Data Name(\\)?=(\'|")SubjectDomainName(\'|")>({src_domain}({domain}[^<]+))</Data>'] |
| edit_regex_field | user |  | ['<Data Name(\\)?=(\'|")SubjectUserName(\'|")>({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))</Data>'] |
| added_regex_field | src_domain |  | ['<Data Name(\\)?=(\'|")SubjectDomainName(\'|")>({src_domain}({domain}[^<]+))</Data>'] |
| added_regex_field | src_user |  | ['<Data Name(\\)?=(\'|")SubjectUserName(\'|")>({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))</Data>'] |
| removed_attribute | DupFields |  | N/A |