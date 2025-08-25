# Code Changes for symantec-vip-json-app-checkforchallenge (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed | Conditions |  | ['ACTION_TYPE: "', 'MESSAGE_CODE: "', 'SUCCESS: "', 'TRANSACTION_TIMESTAMP: "'] |
| edit_regex_field | action |  | ['ACTION_TYPE:\s*"*({action}[^"]+)'] |
| edit_regex_field | email_address |  | ['CUST_LOGIN_ID:\s*"*(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| edit_regex_field | email_domain |  | ['CUST_LOGIN_ID:\s*"*(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| edit_regex_field | result |  | ['SUCCESS:\s*"*({result}[^"]+)'] |
| edit_regex_field | src_ip |  | ['CLIENT_IP:\s*"*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?'] |
| edit_regex_field | src_port |  | ['CLIENT_IP:\s*"*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?'] |
| edit_regex_field | time |  | ['TRANSACTION_TIMESTAMP:\s*"*({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)'] |
| edit_regex_field | user |  | ['CUST_LOGIN_ID:\s*"*(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| edit_regex_field | user_agent |  | ['CLIENT_BROWSER_DATA:\s*"*({user_agent}[^"]+)'] |