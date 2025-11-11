# Code Changes for microsoft-evsecurity-xml-ds-object-modify-success-5136 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['attribute', 'attribute_value', 'dest_host', 'domain', 'ds_name', 'ds_object_dn', 'ds_type', 'event_code', 'event_name', 'host', 'login_id', 'object_type', 'operation_type', 'run_level', 'src_domain', 'src_user', 'time', 'user'] |
| edit_regex_field | domain |  | ['<Data Name\\*=(\'|")SubjectDomainName(\'|")>\s*({src_domain}({domain}[^<]+?))\s*</Data>'] |
| edit_regex_field | user |  | ['<Data Name\\*=(\'|")SubjectUserName(\'|")>\s*((?i)(LOCAL SYSTEM|anonymous logon|LOCAL SERVICE|SYSTEM)|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\s*</Data>'] |
| added_regex_field | src_domain |  | ['<Data Name\\*=(\'|")SubjectDomainName(\'|")>\s*({src_domain}({domain}[^<]+?))\s*</Data>'] |
| added_regex_field | src_user |  | ['<Data Name\\*=(\'|")SubjectUserName(\'|")>\s*((?i)(LOCAL SYSTEM|anonymous logon|LOCAL SERVICE|SYSTEM)|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\s*</Data>'] |
| removed_attribute | DupFields |  | N/A |