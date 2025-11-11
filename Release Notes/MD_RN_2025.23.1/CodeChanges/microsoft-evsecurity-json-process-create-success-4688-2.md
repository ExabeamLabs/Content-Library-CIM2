# Code Changes for microsoft-evsecurity-json-process-create-success-4688-2 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['domain', 'event_code', 'event_name', 'host', 'login_id', 'process_command_line', 'process_dir', 'process_guid', 'process_name', 'process_path', 'src_domain', 'src_host', 'src_user', 'time', 'user'] |
| edit_regex_field | domain |  | ['"Account"*:"*(({src_domain}({domain}[^"]+?))[\\\/]+)?({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))"', '"SubjectDomainName"*:"*(-|({src_domain}({domain}[^"]+?)))"', 'exa_json_path=$.Account,exa_regex=(({src_domain}({domain}[^"]+?))[\\\/]+)?({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| edit_regex_field | user |  | ['"Account"*:"*(({src_domain}({domain}[^"]+?))[\\\/]+)?({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))"', '"SubjectUserName"*:"*(-|SYSTEM|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))"', 'exa_json_path=$.Account,exa_regex=(({src_domain}({domain}[^"]+?))[\\\/]+)?({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| added_regex_field | src_domain |  | ['"Account"*:"*(({src_domain}({domain}[^"]+?))[\\\/]+)?({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))"', '"SubjectDomainName"*:"*(-|({src_domain}({domain}[^"]+?)))"', 'exa_json_path=$.Account,exa_regex=(({src_domain}({domain}[^"]+?))[\\\/]+)?({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| added_regex_field | src_user |  | ['"Account"*:"*(({src_domain}({domain}[^"]+?))[\\\/]+)?({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))"', '"SubjectUserName"*:"*(-|SYSTEM|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))"', 'exa_json_path=$.Account,exa_regex=(({src_domain}({domain}[^"]+?))[\\\/]+)?({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| removed_attribute | DupFields |  | N/A |