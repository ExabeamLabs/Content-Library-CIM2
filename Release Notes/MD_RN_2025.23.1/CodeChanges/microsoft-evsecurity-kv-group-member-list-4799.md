# Code Changes for microsoft-evsecurity-kv-group-member-list-4799 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['domain', 'event_code', 'event_name', 'group_domain', 'group_id', 'group_name', 'host', 'login_id', 'process_dir', 'process_id', 'process_name', 'process_path', 'src_domain', 'src_user', 'time', 'user', 'user_sid'] |
| edit_regex_field | domain |  | ['Subject:\s*[^"]+?Account Domain:\s*(-|({src_domain}({domain}[^\s]+)))'] |
| edit_regex_field | user |  | ['Subject:\s*[^"]+?Account Name:\s*(-|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\s*\w+\s\w+:', 'exa_json_path=$..SubjectUserName,exa_regex=(SYSTEM|ANONYMOUS LOGON|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))'] |
| added_regex_field | src_domain |  | ['Subject:\s*[^"]+?Account Domain:\s*(-|({src_domain}({domain}[^\s]+)))'] |
| added_regex_field | src_user |  | ['Subject:\s*[^"]+?Account Name:\s*(-|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\s*\w+\s\w+:', 'exa_json_path=$..SubjectUserName,exa_regex=(SYSTEM|ANONYMOUS LOGON|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))'] |
| removed_attribute | DupFields |  | N/A |