# Code Changes for microsoft-evsecurity-xml-ds-object-activity-success-4662 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'access_list', 'access_mask', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'object_name', 'object_server', 'object_type', 'operation', 'properties', 'result', 'run_level', 'src_domain', 'src_host', 'src_user', 'time', 'user', 'user_sid'] |
| edit_regex_field | domain |  | ['<Data Name(\\)?=(\'|")SubjectDomainName(\'|")>(-|({src_domain}({domain}[^<]+)))'] |
| edit_regex_field | user |  | ['<Data Name(\\)?=(\'|")SubjectUserName(\'|")>(-|CN=[^<]+|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))<'] |
| added_regex_field | src_domain |  | ['<Data Name(\\)?=(\'|")SubjectDomainName(\'|")>(-|({src_domain}({domain}[^<]+)))'] |
| added_regex_field | src_user |  | ['<Data Name(\\)?=(\'|")SubjectUserName(\'|")>(-|CN=[^<]+|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))<'] |
| removed_attribute | DupFields |  | N/A |