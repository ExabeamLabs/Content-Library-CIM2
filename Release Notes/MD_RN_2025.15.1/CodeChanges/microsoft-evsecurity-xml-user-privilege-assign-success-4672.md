# Code Changes for microsoft-evsecurity-xml-user-privilege-assign-success-4672 (Parser)

| Code Change | Field Name | 2025.14.1 | 2025.15.1 |
|-------------|------------|-----------|------------|
| edit_regex_field | login_id | ['<Data Name(\\\/)?=(\'|")SubjectLogonId(\'|")>({login_id}[^<]+)</Data>', 'SubjectLogonId(\'|")>({login_id}[^<]+)'] | ['<Data Name(\\\/)?=(\'|")SubjectLogonId(\'|")>({login_id}[^<]+?)</Data>', 'SubjectLogonId(\'|")>({login_id}[^<]+)'] |