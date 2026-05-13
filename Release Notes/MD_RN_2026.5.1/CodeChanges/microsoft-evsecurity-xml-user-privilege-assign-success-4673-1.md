# Code Changes for microsoft-evsecurity-xml-user-privilege-assign-success-4673-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'dest_host', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'object_server', 'privileges', 'process_dir', 'process_name', 'process_path', 'result', 'run_level', 'src_domain', 'src_user', 'time', 'user', 'user_sid'] |
| edit_regex_field | domain |  | ['<Data Name[\\\/]*=(\'|")SubjectDomainName(\'|")>({domain}({src_domain}[^<]+?))</Data>'] |
| edit_regex_field | user |  | ['<Data Name[\\\/]*=(\'|")SubjectUserName(\'|")>({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))</Data>'] |
| added_regex_field | user_sid |  | ['<Data Name[\\\/]*=(\'|")SubjectUserSid(\'|")>\s*({user_sid}S-[^\s"<>]+)<\/Data>'] |