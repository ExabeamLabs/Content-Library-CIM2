# Code Changes for microsoft-evsecurity-xml-group-member-remove-success-eventid (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_id', 'dest_host', 'dest_user', 'dest_user_full_name', 'dest_user_sid', 'domain', 'event_code', 'event_name', 'group_domain', 'group_id', 'group_name', 'group_type', 'host', 'login_id', 'member', 'run_level', 'src_domain', 'src_user', 'time', 'user', 'user_dn', 'user_ou', 'user_sid'] |
| edit_regex_field | domain |  | ['<Data Name=(\'|")SubjectDomainName(\'|")>({src_domain}({domain}[^"\s<]+))<'] |
| edit_regex_field | member |  | ['<Data Name="MemberName(">|":")CN\\?=({member}[^>]+)<\/Data>', '<Data Name=(\'|")MemberName(\'|")>(-|({member}({user_dn}[^<]+)))<'] |
| edit_regex_field | user |  | ['<Data Name=(\'|")SubjectUserName(\'|")>({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))<'] |
| edit_regex_field | user_dn |  | ['<Data Name=(\'|")MemberName(\'|")>(-|({member}({user_dn}[^<]+)))<'] |
| added_regex_field | src_domain |  | ['<Data Name=(\'|")SubjectDomainName(\'|")>({src_domain}({domain}[^"\s<]+))<'] |
| added_regex_field | src_user |  | ['<Data Name=(\'|")SubjectUserName(\'|")>({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))<'] |
| removed_attribute | DupFields |  | N/A |