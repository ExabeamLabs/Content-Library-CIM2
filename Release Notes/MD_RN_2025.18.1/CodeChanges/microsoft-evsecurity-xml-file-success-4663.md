# Code Changes for microsoft-evsecurity-xml-file-success-4663 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | access |  | ['<Data Name\\*=(\'|")AccessList(\'|")>([^\d\w]+)?({access}[\d\w]+)', 'Accesses:\s*(\\r|\\n|\\t)*({access}[^:]+?)\s*(\\r|\\n|\\t)*Access Mask:'] |
| edit_regex_field | access_mask |  | ['<Data Name\\*=(\'|")AccessMask(\'|")>({access_mask}[^<\s"]+)'] |
| edit_regex_field | domain |  | ['<Data Name\\*=(\'|")SubjectDomainName(\'|")>({domain}[^<]+)<'] |
| edit_regex_field | file_dir |  | ['<Data Name\\*=(\'|")ObjectName(\'|")>(?!\\+REGISTRY)({file_dir}.+?)[\\\/]+(?:[^\\\/]+?)<'] |
| edit_regex_field | file_ext |  | ['<Data Name\\*=(\'|")ObjectName(\'|")>(?!\\+REGISTRY)[^<]+[\\\/]+({file_name}(?:[^<\\\/:]+?)(\.({file_ext}\w+))?|[^\\:<]+)<'] |
| edit_regex_field | file_name |  | ['<Data Name\\*=(\'|")ObjectName(\'|")>(?!\\+REGISTRY)[^<]+[\\\/]+({file_name}(?:[^<\\\/:]+?)(\.({file_ext}\w+))?|[^\\:<]+)<'] |
| edit_regex_field | file_path |  | ['<Data Name\\*=(\'|")ObjectName(\'|")>(({registry_path}\\+REGISTRY[^<]+?({registry_key}[^<\\\/]+))|({file_path}[^<]+))<'] |
| edit_regex_field | file_type |  | ['<Data Name\\*=(\'|")ObjectType(\'|")>({file_type}[^<]+)<'] |
| edit_regex_field | login_id |  | ['<Data Name\\*=(\'|")SubjectLogonId(\'|")>({login_id}[^<]+)<'] |
| edit_regex_field | process_dir |  | ['<Data Name\\*=(\'|")ProcessName(\'|")>({process_path}({process_dir}(?:[^<]+)?[\\\/])?({process_name}[^\\\/\"<]+?))<'] |
| edit_regex_field | process_name |  | ['<Data Name\\*=(\'|")ProcessName(\'|")>({process_path}({process_dir}(?:[^<]+)?[\\\/])?({process_name}[^\\\/\"<]+?))<'] |
| edit_regex_field | process_path |  | ['<Data Name\\*=(\'|")ProcessName(\'|")>({process_path}({process_dir}(?:[^<]+)?[\\\/])?({process_name}[^\\\/\"<]+?))<'] |
| edit_regex_field | registry_key |  | ['<Data Name\\*=(\'|")ObjectName(\'|")>(({registry_path}\\+REGISTRY[^<]+?({registry_key}[^<\\\/]+))|({file_path}[^<]+))<'] |
| edit_regex_field | registry_path |  | ['<Data Name\\*=(\'|")ObjectName(\'|")>(({registry_path}\\+REGISTRY[^<]+?({registry_key}[^<\\\/]+))|({file_path}[^<]+))<'] |
| edit_regex_field | user |  | ['<Data Name\\*=(\'|")SubjectUserName(\'|")>({user}[\w\.\-\!\#\^\~]{1,40}\$?)<'] |
| edit_regex_field | user_sid |  | ['<Data Name\\*=(\'|")SubjectUserSid(\'|")>(?:NONE_MAPPED|({user_sid}[^<]+))<'] |