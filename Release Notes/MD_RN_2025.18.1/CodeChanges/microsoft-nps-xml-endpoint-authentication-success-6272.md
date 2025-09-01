# Code Changes for microsoft-nps-xml-endpoint-authentication-success-6272 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | access_type |  | ['(\'|")QuarantineState(\'|")>(?:-|({access_type}[^\<]+))'] |
| edit_regex_field | auth_server |  | ['(\'|")AuthenticationProvider(\'|")>(?:-|({auth_server}[^\<]+))'] |
| edit_regex_field | auth_type |  | ['(\'|")EAPType(\'|")>(?:-|({auth_type}[^\<]+))'] |
| edit_regex_field | dest_ip |  | ['(\'|")NASIPv4Address(\'|")>({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?', '(\'|")NASIPv6Address(\'|")>({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?'] |
| edit_regex_field | dest_port |  | ['(\'|")NASIPv4Address(\'|")>({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?', '(\'|")NASIPv6Address(\'|")>({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?'] |
| edit_regex_field | domain |  | ['(\'|")FullyQualifiedSubjectUserName(\'|")>(({domain}[^\\]+)\\+)?(?:-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))', '(\'|")SubjectDomainName(\'|")>(?:-|({domain}[^\s\<]+))', '(\'|")SubjectUserName(\'|")>(?:({user_type}host)/)?(({domain}[^\\]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)'] |
| edit_regex_field | location |  | ['(\'|")NASIdentifier(\'|")>(?:-|({location}[\w\-.]+))'] |
| edit_regex_field | src_domain |  | ['(\'|")SubjectDomainName(\'|")>(?:-|({src_domain}[^\s\<]+))', '(\'|")SubjectUserName(\'|")>(?:({user_type}host)/)?(({src_domain}[^\\]+)\\+)?({src_user}[\w\.\-\!\#\^\~]{1,40}\$?)'] |
| edit_regex_field | src_mac |  | ['(\'|")CallingStationID(\'|")>(?:-|({src_mac}[^\<]+))'] |
| edit_regex_field | src_user |  | ['(\'|")SubjectUserName(\'|")>(?:({user_type}host)/)?(({src_domain}[^\\]+)\\+)?({src_user}[\w\.\-\!\#\^\~]{1,40}\$?)'] |
| edit_regex_field | time |  | ['SystemTime=(\'|")({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d)'] |
| edit_regex_field | user |  | ['(\'|")FullyQualifiedSubjectUserName(\'|")>(({domain}[^\\]+)\\+)?(?:-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))', '(\'|")SubjectUserName(\'|")>(?:({user_type}host)/)?(({domain}[^\\]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)'] |
| edit_regex_field | user_type |  | ['(\'|")FullyQualifiedSubjectMachineName(\'|")>(?:-|({user_type}.+?))(\/[^\/\s]+)?<', '(\'|")SubjectUserName(\'|")>(?:({user_type}host)/)?(({domain}[^\\]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)', '(\'|")SubjectUserName(\'|")>(?:({user_type}host)/)?(({src_domain}[^\\]+)\\+)?({src_user}[\w\.\-\!\#\^\~]{1,40}\$?)'] |