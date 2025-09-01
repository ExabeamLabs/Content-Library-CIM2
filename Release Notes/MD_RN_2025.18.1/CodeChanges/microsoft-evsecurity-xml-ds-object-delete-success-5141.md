# Code Changes for microsoft-evsecurity-xml-ds-object-delete-success-5141 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | domain |  | ['<Data Name\\*=(\'|")SubjectDomainName(\'|")>(|({domain}[^<]+?))</Data>'] |
| edit_regex_field | ds_name |  | ['<Data Name\\*=(\'|")DSName(\'|")>(|({ds_name}[^<]+?))</Data>'] |
| edit_regex_field | ds_object_dn |  | ['<Data Name\\*=(\'|")ObjectDN(\'|")>(|({ds_object_dn}[^<]+?))</Data>'] |
| edit_regex_field | ds_type |  | ['<Data Name\\*=(\'|")DSType(\'|")>(|({ds_type}[^<]+?))</Data>'] |
| edit_regex_field | login_id |  | ['<Data Name\\*=(\'|")SubjectLogonId(\'|")>(|({login_id}[^<]+?))</Data>'] |
| edit_regex_field | object_type |  | ['<Data Name\\*=(\'|")ObjectClass(\'|")>(|({object_type}[^<]+?))</Data>'] |
| edit_regex_field | user |  | ['<Data Name\\*=(\'|")SubjectUserName(\'|")>(|({user}[\w\.\-\!\#\^\~]{1,40}\$?))</Data>'] |
| edit_regex_field | user_sid |  | ['<Data Name\\*=(\'|")SubjectUserSid(\'|")>(|({user_sid}[^<]+?))</Data>'] |