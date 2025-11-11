# Code Changes for microsoft-evsecurity-cef-user-modify-4717 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access_type', 'dest_domain', 'dest_login_id', 'dest_user', 'dest_user_full_name', 'dest_user_sid', 'domain', 'event_code', 'event_name', 'file_path', 'host', 'key_name', 'key_type', 'login_id', 'operation', 'process_dir', 'process_id', 'process_name', 'process_path', 'provider_name', 'return_code', 'run_level', 'src_domain', 'src_user', 'time', 'user', 'user_sid'] |
| edit_regex_field | domain |  | ['<Data Name[^<>]+?SubjectDomainName[^<>]+?>({src_domain}({domain}[^<>]+?))</Data>'] |
| edit_regex_field | user |  | ['<Data Name[^<>]+?SubjectUserName[^<>]+?>({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))</Data>'] |
| added_regex_field | src_domain |  | ['<Data Name[^<>]+?SubjectDomainName[^<>]+?>({src_domain}({domain}[^<>]+?))</Data>'] |
| added_regex_field | src_user |  | ['<Data Name[^<>]+?SubjectUserName[^<>]+?>({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))</Data>'] |
| removed_attribute | DupFields |  | N/A |