# Code Changes for microsoft-evsecurity-xml-ds-object-delete-success-5141 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['domain', 'ds_name', 'ds_object_dn', 'ds_type', 'event_code', 'event_name', 'host', 'login_id', 'object_type', 'result', 'run_level', 'src_domain', 'src_user', 'time', 'user', 'user_sid'] |
| edit_regex_field | domain |  | ['<Data Name\\*=(\'|")SubjectDomainName(\'|")>(|({src_domain}({domain}[^<]+?)))</Data>'] |
| edit_regex_field | user |  | ['<Data Name\\*=(\'|")SubjectUserName(\'|")>(|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))</Data>'] |
| added_regex_field | src_domain |  | ['<Data Name\\*=(\'|")SubjectDomainName(\'|")>(|({src_domain}({domain}[^<]+?)))</Data>'] |
| added_regex_field | src_user |  | ['<Data Name\\*=(\'|")SubjectUserName(\'|")>(|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))</Data>'] |
| removed_attribute | DupFields |  | N/A |