# Code Changes for microsoft-evsecurity-xml-configuration-modify-success-4742 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_id', 'additional_info', 'dest_domain', 'dest_host', 'dest_ip', 'dest_port', 'dest_user', 'dest_user_sid', 'domain', 'event_code', 'host', 'login_id', 'new_value', 'old_value', 'process_guid', 'process_id', 'provider_name', 'run_level', 'sid_domain', 'src_domain', 'src_ip', 'src_port', 'src_user', 'time', 'uac_status', 'user', 'user_dn', 'user_ou', 'user_sid'] |
| edit_regex_field | domain |  | ['<Data Name(\\)?=(\'|")SubjectDomainName(\'|")>({src_domain}({domain}[^<]+))</Data>'] |
| edit_regex_field | user |  | ['<Data Name(\\)?=(\'|")SubjectUserName(\'|")>({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))</Data>'] |
| added_regex_field | src_domain |  | ['<Data Name(\\)?=(\'|")SubjectDomainName(\'|")>({src_domain}({domain}[^<]+))</Data>'] |
| added_regex_field | src_user |  | ['<Data Name(\\)?=(\'|")SubjectUserName(\'|")>({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))</Data>'] |
| removed_attribute | DupFields |  | N/A |