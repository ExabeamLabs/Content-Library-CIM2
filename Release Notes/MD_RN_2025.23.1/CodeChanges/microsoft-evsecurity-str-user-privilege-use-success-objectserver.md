# Code Changes for microsoft-evsecurity-str-user-privilege-use-success-objectserver (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'domain', 'event_code', 'handle_id', 'host', 'login_id', 'object', 'object_server', 'privileges', 'process_dir', 'process_id', 'process_name', 'process_path', 'result', 'src_domain', 'src_user', 'time', 'user'] |
| edit_regex_field | domain |  | ['SubjectDomainName:({src_domain}({domain}[^,]+)),'] |
| edit_regex_field | host |  | ['({dest_host}({host}[\w\-.]+))\s+Sensitive Privilege Use'] |
| edit_regex_field | user |  | ['SubjectUserName:({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)),'] |
| added_regex_field | dest_host |  | ['({dest_host}({host}[\w\-.]+))\s+Sensitive Privilege Use'] |
| added_regex_field | src_domain |  | ['SubjectDomainName:({src_domain}({domain}[^,]+)),'] |
| added_regex_field | src_user |  | ['SubjectUserName:({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)),'] |
| removed_attribute | DupFields |  | N/A |