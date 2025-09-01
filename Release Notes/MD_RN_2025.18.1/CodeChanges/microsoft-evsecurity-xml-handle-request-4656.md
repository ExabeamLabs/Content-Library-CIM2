# Code Changes for microsoft-evsecurity-xml-handle-request-4656 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | login_id |  | ['<Data Name(\\)?=(\'|")SubjectLogonId(\'|")>({login_id}[^<]+)'] |