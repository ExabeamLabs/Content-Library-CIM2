# Code Changes for microsoft-evsecurity-json-ds-object-modify-success-4738 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'category', 'dest_domain', 'dest_user', 'dest_user_sid', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'result', 'severity', 'src_domain', 'src_user', 'time', 'user', 'user_sid'] |
| edit_regex_field | additional_info |  | ['"+Message\\?"+:\\?"+({additional_info}[^"\\\.]+?)"', '({additional_info}({event_name}A user account was changed))'] |
| edit_regex_field | domain |  | ['"SubjectDomainName\\?":\\?"({src_domain}({domain}[^"\\]+))'] |
| edit_regex_field | event_name |  | ['({additional_info}({event_name}A user account was changed))'] |
| edit_regex_field | user |  | ['"SubjectUserName\\?":\\?"({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| added_regex_field | src_domain |  | ['"SubjectDomainName\\?":\\?"({src_domain}({domain}[^"\\]+))'] |
| added_regex_field | src_user |  | ['"SubjectUserName\\?":\\?"({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| removed_attribute | DupFields |  | N/A |