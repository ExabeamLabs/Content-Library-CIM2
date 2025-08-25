# Code Changes for microsoft-evsecurity-xml-endpoint-login-success-4624-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | auth_package |  | ['<Data Name\\*=(\'|")AuthenticationPackageName(\'|")>({auth_package}[^<]+)<', '<Data Name\\*=(\'|")LmPackageName(\'|")>(-|({auth_package}[^<]+))<'] |
| edit_regex_field | auth_process |  | ['<Data Name\\*=(\'|")LogonProcessName(\'|")>({auth_process}[^\s<]+)'] |
| edit_regex_field | domain |  | ['<Data Name\\*=(\'|")TargetDomainName(\'|")>(-|({domain}[^<]+))<', '<Data Name\\*=(\'|")TargetUserName(\'|")>(-|({user_upn}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({domain}[^\]\s"\\,;\|]+(\.[^\]\s"\\,;\|]+)?))|({full_name}[^\s<]+\s[^<]+)|(SYSTEM|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))<\/Data>'] |
| edit_regex_field | full_name |  | ['<Data Name\\*=(\'|")TargetUserName(\'|")>(-|({user_upn}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({domain}[^\]\s"\\,;\|]+(\.[^\]\s"\\,;\|]+)?))|({full_name}[^\s<]+\s[^<]+)|(SYSTEM|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))<\/Data>'] |
| edit_regex_field | key_length |  | ['<Data Name\\*=(\'|")KeyLength(\'|")>({key_length}\d+)<'] |
| edit_regex_field | login_id |  | ['<Data Name\\*=(\'|")TargetLogonId(\'|")>({login_id}[^<]+)<'] |
| edit_regex_field | login_type |  | ['<Data Name\\*=(\'|")LogonType(\'|")>({login_type}\d+)<'] |
| edit_regex_field | process_dir |  | ['<Data Name\\*=(\'|")ProcessName(\'|")>(?:-|({process_path}({process_dir}[^<>]*?[\\\/]+)?({process_name}[^<>\\\/]+)))<'] |
| edit_regex_field | process_id |  | ['<Data Name\\*=(\'|")ProcessId(\'|")>({process_id}[^<]+?)\s*<'] |
| edit_regex_field | process_name |  | ['<Data Name\\*=(\'|")ProcessName(\'|")>(?:-|({process_path}({process_dir}[^<>]*?[\\\/]+)?({process_name}[^<>\\\/]+)))<'] |
| edit_regex_field | process_path |  | ['<Data Name\\*=(\'|")ProcessName(\'|")>(?:-|({process_path}({process_dir}[^<>]*?[\\\/]+)?({process_name}[^<>\\\/]+)))<'] |
| edit_regex_field | provider_name |  | ['<Provider Name\\*=(\'|")({provider_name}[^\'\"]+)'] |
| edit_regex_field | src_host_windows |  | ['<Data Name\\*=(\'|")WorkstationName(\'|")>([A-Fa-f:\d.]+|-|({src_host_windows}[^<]+?))\s*<'] |
| edit_regex_field | src_ip |  | ['<Data Name\\*=(\'|")IpAddress"[^<>]*?>(?:-|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)<'] |
| edit_regex_field | src_port |  | ["<Data Name\\*='IpPort'>({src_port}\d+)", '<Data Name\\*=(\'|")IpAddress"[^<>]*?>(?:-|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)<'] |
| edit_regex_field | subject_sid |  | ['<Data Name\\*=(\'|")SubjectUserSid(\'|")>({subject_sid}[^<]+)<'] |
| edit_regex_field | time |  | ['SystemTime\\*=(\'|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)'] |
| edit_regex_field | user |  | ['<Data Name\\*=(\'|")TargetUserName(\'|")>(-|({user_upn}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({domain}[^\]\s"\\,;\|]+(\.[^\]\s"\\,;\|]+)?))|({full_name}[^\s<]+\s[^<]+)|(SYSTEM|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))<\/Data>'] |
| edit_regex_field | user_sid |  | ['<Data Name\\*=(\'|")TargetUserSid(\'|")>({user_sid}[^<]+)<'] |
| edit_regex_field | user_upn |  | ['<Data Name\\*=(\'|")TargetUserName(\'|")>(-|({user_upn}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({domain}[^\]\s"\\,;\|]+(\.[^\]\s"\\,;\|]+)?))|({full_name}[^\s<]+\s[^<]+)|(SYSTEM|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))<\/Data>'] |