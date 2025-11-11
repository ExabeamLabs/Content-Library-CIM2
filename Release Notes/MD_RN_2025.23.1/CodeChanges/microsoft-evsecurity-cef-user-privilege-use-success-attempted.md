# Code Changes for microsoft-evsecurity-cef-user-privilege-use-success-attempted (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'domain', 'event_code', 'event_id', 'event_name', 'host', 'login_id', 'object_server', 'privileges', 'process_dir', 'process_name', 'process_path', 'result', 'src_domain', 'src_user', 'time', 'user', 'user_sid'] |
| edit_regex_field | domain |  | ['"subjectDomainName":\"(-|({src_domain}({domain}[^\s\"]+)))"'] |
| edit_regex_field | host |  | ['"computer":\"({dest_host}({host}[\w\-.]+))'] |
| edit_regex_field | user |  | ['"subjectUserName":\"(-|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))"'] |
| added_regex_field | dest_host |  | ['"computer":\"({dest_host}({host}[\w\-.]+))'] |
| added_regex_field | src_domain |  | ['"subjectDomainName":\"(-|({src_domain}({domain}[^\s\"]+)))"'] |
| added_regex_field | src_user |  | ['"subjectUserName":\"(-|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))"'] |
| removed_attribute | DupFields |  | N/A |