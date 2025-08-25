# Code Changes for microsoft-evsecurity-json-endpoint-login-4768-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| COULD_NOT_COMPARE | TimeFormat |  | ['yyyy-MM-dd HH:mm:ss', 'yyyy-MM-dd HH:mm:ss Z'] |
| changed | Conditions |  | ['"Channel":"Security"', '"Microsoft-Windows-Security-Auditing"', 'EventID":4768'] |
| edit_regex_field | event_name |  | ['"Category"+:"+({event_name}[^"]+)', 'exa_regex=({event_name}A Kerberos authentication ticket (TGT) was requested)'] |
| edit_regex_field | result_code |  | ['"Status"+:"+({result_code}[^"]+)', 'exa_regex=Result Code:\s*({result_code}[^\s]+)'] |
| edit_regex_field | service_name |  | ['"ServiceName"+:"+({service_name}[^"]+)', 'exa_regex=Service Name:\s*({service_name}[^\s]+)'] |
| edit_regex_field | src_ip |  | ['IpAddress"+:"+(::[\w]+:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?', 'exa_regex=Client Address:\s+(::[\w]+:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?'] |
| edit_regex_field | src_port |  | ['"IpPort"+:"+({src_port}\d+)', 'IpAddress"+:"+(::[\w]+:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?', 'exa_regex=Client Address:\s+(::[\w]+:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?', 'exa_regex=Client Port:\s*({src_port}\d+)'] |
| edit_regex_field | ticket_encryption_type |  | ['"TicketEncryptionType":"({ticket_encryption_type}[^"]+)', 'exa_regex=Ticket Encryption Type:\s*({ticket_encryption_type}[^\s]+)'] |
| edit_regex_field | ticket_options |  | ['"TicketOptions"+:"+({ticket_options}[^"]+)', 'exa_regex=Ticket Options:\s*({ticket_options}[^\s]+)'] |
| edit_regex_field | user |  | ['"TargetUserName"+:"+({user}[\w\.\-\!\#\^\~]{1,40}\$?)', 'exa_regex=Account Name:\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)'] |
| edit_regex_field | user_sid |  | ['TargetSid"+:"+({user_sid}[^"]+)"', 'exa_regex=User ID:\s*({user_sid}S-[^\s]+)'] |
| added_attribute | ExtractionType |  | json |