# Code Changes for microsoft-evsecurity-xml-endpoint-login-4769-2 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | dest_host |  | ['Service Name(:|=)\s*(\\r|\\n|\\t)*({dest_host}[\w\-\.]+)\$(\\r|\\n|\\t)*[\s;]*Service ID'] |
| edit_regex_field | domain |  | ['Account Name(:|=)\s*(\\r|\\n|\\t)*({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[\w._\-]+))?(\\r|\\n|\\t)*[\s;]*Account Domain(:|=)'] |
| edit_regex_field | failure_code |  | ['Failure Code(:|=)\s*(\\r|\\n|\\t)*({failure_code}({result_code}[^\s:;\\]+))(\\r|\\n|\\t)*[\s;]*[\w\s]+(:|=)'] |
| edit_regex_field | result_code |  | ['Failure Code(:|=)\s*(\\r|\\n|\\t)*({failure_code}({result_code}[^\s:;\\]+))(\\r|\\n|\\t)*[\s;]*[\w\s]+(:|=)'] |
| edit_regex_field | service_name |  | ['Service Name(:|=)\s*(\\r|\\n|\\t)*({service_name}[^\s;]+?)(\\r|\\n|\\t)*[\s;]*Service ID'] |
| edit_regex_field | src_ip |  | ['Client Address(:|=)\s*(\\r|\\n|\\t)*(::[\w]+:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?'] |
| edit_regex_field | src_port |  | ['Client Address(:|=)\s*(\\r|\\n|\\t)*(::[\w]+:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?'] |
| edit_regex_field | ticket_encryption_type |  | ['Ticket Encryption Type(:|=)\s*(\\r|\\n|\\t)*({ticket_encryption_type}[^\s\\;]+?)(\\r|\\n\\t)*[\s;]*Failure Code(:|=)'] |
| edit_regex_field | ticket_options |  | ['Ticket Options(:|=)\s*(\\r|\\n|\\t)*({ticket_options}[^\s\\;]+?)[\s;]*(\\r|\\n|\\t)*Ticket Encryption Type(:|=)'] |
| edit_regex_field | user |  | ['Account Name(:|=)\s*(\\r|\\n|\\t)*({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[\w._\-]+))?(\\r|\\n|\\t)*[\s;]*Account Domain(:|=)'] |
| edit_attribute | legacy_activity_type |  | ['authentication-failed', 'remote-access'] |