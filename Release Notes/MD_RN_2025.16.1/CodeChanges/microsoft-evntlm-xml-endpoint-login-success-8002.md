# Code Changes for microsoft-evntlm-xml-endpoint-login-success-8002 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | domain |  | ['<Data Name=(\'|")ClientDomainName(\'|")>(\((?i)NULL\)|({domain}[^<]+))<'] |
| edit_regex_field | login_type |  | ['<Data Name=(\'|")LogonType(\'|")>({login_type}\d+)<\/Data>'] |
| edit_regex_field | process_dir |  | ['<Data Name=(\'|")ProcessName(\'|")>({process_path}({process_dir}[^<\/]+?)\\+({process_name}[^<\\]+))<'] |
| edit_regex_field | process_name |  | ['<Data Name=(\'|")ProcessName(\'|")>({process_path}({process_dir}[^<\/]+?)\\+({process_name}[^<\\]+))<'] |
| edit_regex_field | process_path |  | ['<Data Name=(\'|")ProcessName(\'|")>({process_path}({process_dir}[^<\/]+?)\\+({process_name}[^<\\]+))<'] |
| edit_regex_field | src_host |  | ['<Data Name=(\'|")Workstation(\'|")>(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|(?:(?!NULL)(Unknown|({src_host}[^\s.]+))(\.[^\s]+)?))<\/Data>'] |
| edit_regex_field | src_ip |  | ['<Data Name=(\'|")Workstation(\'|")>(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|(?:(?!NULL)(Unknown|({src_host}[^\s.]+))(\.[^\s]+)?))<\/Data>'] |
| edit_regex_field | user |  | ['<Data Name=(\'|")ClientUserName(\'|")>(\((?i)NULL\)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))<\/Data>'] |
| edit_regex_field | user_sid |  | ['Security UserID=(\'|")({user_sid}[^\'\/>"]+)'] |