# Code Changes for microsoft-evsecurity-xml-user-delete-success-4743-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_domain', 'dest_user', 'domain', 'event_code', 'event_id', 'host', 'login_id', 'process_guid', 'process_id', 'provider_name', 'result', 'run_level', 'src_domain', 'src_user', 'sub_category', 'thread_id', 'time', 'user', 'user_sid'] |
| edit_regex_field | domain |  | ['<Data Name[^<>]+?SubjectDomainName[^<>]+?>({src_domain}({domain}[^<>]+?))</Data>'] |
| edit_regex_field | user |  | ['<Data Name[^<>]+?SubjectUserName[^<>]+?>({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))</Data>'] |
| added_regex_field | src_domain |  | ['<Data Name[^<>]+?SubjectDomainName[^<>]+?>({src_domain}({domain}[^<>]+?))</Data>'] |
| added_regex_field | src_user |  | ['<Data Name[^<>]+?SubjectUserName[^<>]+?>({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))</Data>'] |
| removed_attribute | DupFields |  | N/A |