# Code Changes for microsoft-evsecurity-xml-ds-object-create-success-5137 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | domain |  | ['<Data Name\\*=(\'|")SubjectDomainName(\'|")>(|({domain}[^<]+?))</Data>'] |
| edit_regex_field | login_id |  | ['<Data Name\\*=(\'|")SubjectLogonId(\'|")>(|({login_id}[^<]+?))</Data>'] |
| edit_regex_field | object_type |  | ['<Data Name\\*=(\'|")ObjectClass(\'|")>(|({object_type}[^<]+?))</Data>'] |
| edit_regex_field | time |  | ['<TimeCreated SystemTime(\\)?=(\'|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)', '<TimeCreated SystemTime=(\'|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d\d\d\d\d\d\dZ)'] |
| edit_regex_field | user |  | ['<Data Name\\*=(\'|")SubjectUserName(\'|")>(|({user}[\w\.\-\!\#\^\~]{1,40}\$?))</Data>'] |
| edit_regex_field | user_sid |  | ['<Data Name\\*=(\'|")SubjectUserSid(\'|")>(|({user_sid}[^<]+?))</Data>'] |