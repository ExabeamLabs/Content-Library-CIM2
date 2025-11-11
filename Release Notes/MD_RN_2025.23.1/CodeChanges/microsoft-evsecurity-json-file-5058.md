# Code Changes for microsoft-evsecurity-json-file-5058 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['activity_id', 'additional_info', 'category', 'dest_host', 'domain', 'event_code', 'event_name', 'file_path', 'host', 'key_name', 'log_source', 'login_id', 'operation', 'process_guid', 'process_id', 'result', 'src_domain', 'src_user', 'time', 'user', 'user_sid'] |
| edit_regex_field | host |  | ['"+(Hostname|Computer)"+:"+({dest_host}({host}[^"]+))"+'] |
| edit_regex_field | user |  | ['"SubjectUserName"+:"+({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))"'] |
| added_regex_field | dest_host |  | ['"+(Hostname|Computer)"+:"+({dest_host}({host}[^"]+))"+'] |
| added_regex_field | domain |  | ['"SubjectDomainName"+:"+({src_domain}({domain}[^"]+))"'] |
| added_regex_field | src_domain |  | ['"SubjectDomainName"+:"+({src_domain}({domain}[^"]+))"'] |
| added_regex_field | src_user |  | ['"SubjectUserName"+:"+({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))"'] |
| removed_attribute | DupFields |  | N/A |