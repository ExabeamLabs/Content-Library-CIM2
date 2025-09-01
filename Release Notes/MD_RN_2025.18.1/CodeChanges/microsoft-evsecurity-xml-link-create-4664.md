# Code Changes for microsoft-evsecurity-xml-link-create-4664 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | domain |  | ['(\'|")SubjectDomainName(\'|")>({domain}[^\'<\s"]+)<'] |
| edit_regex_field | file_dir |  | ['(\'|")FileName(\'|")>(|({file_path}({file_dir}[^"<]*?)[\\\/]*({file_name}[^\\\/"<]+?(\.({file_ext}[^\\\/\.\s"<]+))?)))<'] |
| edit_regex_field | file_ext |  | ['(\'|")FileName(\'|")>(|({file_path}({file_dir}[^"<]*?)[\\\/]*({file_name}[^\\\/"<]+?(\.({file_ext}[^\\\/\.\s"<]+))?)))<'] |
| edit_regex_field | file_name |  | ['(\'|")FileName(\'|")>(|({file_path}({file_dir}[^"<]*?)[\\\/]*({file_name}[^\\\/"<]+?(\.({file_ext}[^\\\/\.\s"<]+))?)))<'] |
| edit_regex_field | file_path |  | ['(\'|")FileName(\'|")>(|({file_path}({file_dir}[^"<]*?)[\\\/]*({file_name}[^\\\/"<]+?(\.({file_ext}[^\\\/\.\s"<]+))?)))<'] |
| edit_regex_field | login_id |  | ['(\'|")SubjectLogonId(\'|")>({login_id}[^\'<\s"]+)<'] |
| edit_regex_field | transaction_id |  | ['(\'|")TransactionId(\'|")>\{?({transaction_id}[^\'<\}"]+)\}?<'] |
| edit_regex_field | user |  | ['(\'|")SubjectUserName(\'|")>({user}[\w\.\-\!\#\^\~]{1,40}\$?)<'] |
| edit_regex_field | user_sid |  | ['(\'|")SubjectUserSid(\'|")>({user_sid}[^\'<\s"]+)<'] |