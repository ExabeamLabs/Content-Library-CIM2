# Code Changes for microsoft-evsecurity-xml-ds-object-move-success-5139 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['domain', 'ds_name', 'ds_object_dn', 'ds_type', 'event_code', 'host', 'login_id', 'object_id', 'object_type', 'run_level', 'src_domain', 'src_ds_object_dn', 'src_user', 'time', 'user', 'user_sid'] |
| edit_regex_field | domain |  | ['<Data Name\\*=(\'|")SubjectDomainName(\'|")>\s*({src_domain}({domain}[^\s]+?))\s*</Data>'] |
| edit_regex_field | src_ds_object_dn |  | ['<Data Name\\*=(\'|")NewObjectDN(\'|")>\s*({ds_object_dn}({src_ds_object_dn}.+?))</Data>\s*'] |
| edit_regex_field | user |  | ['<Data Name\\*=(\'|")SubjectUserName(\'|")>\s*((?i)(LOCAL SYSTEM|anonymous logon|LOCAL SERVICE|SYSTEM)|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\s*</Data>'] |
| added_regex_field | ds_object_dn |  | ['<Data Name\\*=(\'|")NewObjectDN(\'|")>\s*({ds_object_dn}({src_ds_object_dn}.+?))</Data>\s*'] |
| added_regex_field | src_domain |  | ['<Data Name\\*=(\'|")SubjectDomainName(\'|")>\s*({src_domain}({domain}[^\s]+?))\s*</Data>'] |
| added_regex_field | src_user |  | ['<Data Name\\*=(\'|")SubjectUserName(\'|")>\s*((?i)(LOCAL SYSTEM|anonymous logon|LOCAL SERVICE|SYSTEM)|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\s*</Data>'] |
| removed_attribute | DupFields |  | N/A |