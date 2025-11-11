# Code Changes for microsoft-evsecurity-xml-ds-object-activity-success-4662-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['domain', 'event_code', 'event_id', 'event_name', 'handle_id', 'host', 'login_id', 'object_name', 'object_server', 'object_type', 'operation', 'properties', 'run_level', 'src_domain', 'src_user', 'time', 'user', 'user_sid'] |
| edit_regex_field | domain |  | ['(\'|")SubjectDomainName(\'|")>({src_domain}({domain}[^"\s<]+))<'] |
| edit_regex_field | user |  | ['(\'|")SubjectUserName(\'|")>({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))<'] |
| added_regex_field | src_domain |  | ['(\'|")SubjectDomainName(\'|")>({src_domain}({domain}[^"\s<]+))<'] |
| added_regex_field | src_user |  | ['(\'|")SubjectUserName(\'|")>({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))<'] |
| removed_attribute | DupFields |  | N/A |