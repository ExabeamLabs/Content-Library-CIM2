# Code Changes for microsoft-evsecurity-sk4-audit-policy-modify-success-4907 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'dest_host', 'domain', 'event_code', 'event_name', 'handle_id', 'host', 'object', 'object_server', 'object_type', 'src_domain', 'src_ip', 'src_user', 'time', 'user', 'user_sid'] |
| edit_regex_field | domain |  | ["SubjectDomainName':\s+'({src_domain}({domain}[^']+))'"] |
| edit_regex_field | host |  | ["Computer':\s+[^\/]+\/({dest_host}({host}[^']+))'"] |
| edit_regex_field | user |  | ["SubjectUserName':\s+'({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))'"] |
| added_regex_field | dest_host |  | ["Computer':\s+[^\/]+\/({dest_host}({host}[^']+))'"] |
| added_regex_field | src_domain |  | ["SubjectDomainName':\s+'({src_domain}({domain}[^']+))'"] |
| added_regex_field | src_user |  | ["SubjectUserName':\s+'({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))'"] |
| removed_attribute | DupFields |  | N/A |