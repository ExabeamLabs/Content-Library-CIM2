# Code Changes for microsoft-evnps-xml-radius-traffic-success-6272 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed | Conditions |  | ['<Channel>Security</Channel>', '<EventID>6272<', 'SubjectUserName'] |
| edit_regex_field | access_type |  | ['(\'|")QuarantineState(\'|")>(?:-|({access_type}[^\<]+))'] |
| edit_regex_field | auth_server |  | ['(\'|")AuthenticationProvider(\'|")>(?:-|({auth_server}[^\<]+))'] |
| edit_regex_field | auth_type |  | ['(\'|")EAPType(\'|")>(?:-|({auth_type}[^\<]+))'] |
| edit_regex_field | dest_ip |  | ['(\'|")NASIPv4Address(\'|")>({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?', '(\'|")NASIPv6Address(\'|")>({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?'] |
| edit_regex_field | dest_port |  | ['(\'|")NASIPv4Address(\'|")>({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?', '(\'|")NASIPv6Address(\'|")>({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?'] |
| edit_regex_field | domain |  | ['(\'|")SubjectDomainName(\'|")>(-|({domain}[^"\s<]+))<', '(\'|")SubjectUserName(\'|")>(?:({user_type}host)\/)?(-|({domain}[^\\\s"<]+)\\+)?(({user_upn}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@({=domain}[^\]\s"\\,\|]+(\.[^\]\s"\\,\|]+)?))|({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({=domain}[^<]+?))?)<\/'] |
| edit_regex_field | location |  | ['(\'|")NASIdentifier(\'|")>(?:-|({location}[\w\-.]+))'] |
| edit_regex_field | src_mac |  | ['(\'|")CallingStationID(\'|")>(?:-|({src_mac}[^\<]+))'] |
| edit_regex_field | user |  | ['(\'|")SubjectUserName(\'|")>(?:({user_type}host)\/)?(-|({domain}[^\\\s"<]+)\\+)?(({user_upn}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@({=domain}[^\]\s"\\,\|]+(\.[^\]\s"\\,\|]+)?))|({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({=domain}[^<]+?))?)<\/', '\ssuser=\s*(({user_upn}([A-Za-z0-9]+[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+(\.[^\]\s"\\,\|]+)?)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| edit_regex_field | user_sid |  | ['(\'|")SubjectUserSid(\'|")>({user_sid}[^"\s<]+)<'] |
| edit_regex_field | user_type |  | ['(\'|")FullyQualifiedSubjectMachineName(\'|")>(?:-|({user_type}.+?))(\/[^\/\s]+)?<', '(\'|")SubjectUserName(\'|")>(?:({user_type}host)\/)?(-|({domain}[^\\\s"<]+)\\+)?(({user_upn}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@({=domain}[^\]\s"\\,\|]+(\.[^\]\s"\\,\|]+)?))|({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({=domain}[^<]+?))?)<\/'] |
| edit_regex_field | user_upn |  | ['(\'|")SubjectUserName(\'|")>(?:({user_type}host)\/)?(-|({domain}[^\\\s"<]+)\\+)?(({user_upn}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@({=domain}[^\]\s"\\,\|]+(\.[^\]\s"\\,\|]+)?))|({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({=domain}[^<]+?))?)<\/', '\ssuser=\s*(({user_upn}([A-Za-z0-9]+[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+(\.[^\]\s"\\,\|]+)?)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |