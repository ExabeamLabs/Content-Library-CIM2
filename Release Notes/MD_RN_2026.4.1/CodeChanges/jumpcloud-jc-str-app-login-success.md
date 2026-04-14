# Code Changes for jumpcloud-jc-str-app-login-success (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| COULD_NOT_COMPARE | TimeFormat |  | ["yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"] |
| changed_parsed_fields | N/A |  | ['email_address', 'email_domain', 'event_name', 'full_name', 'host', 'process_path', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | user |  | ['User\s+(-|(({email_address}[^@"]+@({email_domain}[^\.]+\.[^"]+?))|({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({full_name}[^~"]+?)))\s+({event_name}logged in)', 'exa_json_path=$.initiated_by.username,exa_regex=({user}[\w\.\-]{1,40}\$?)', 'exa_json_path=$.username,exa_regex=({user}[\w\.\-]{1,40}\$?)'] |
| added_regex_field | host |  | ['exa_json_path=$.system.hostname,exa_regex=({host}[\w\-\.]+)'] |
| added_regex_field | src_ip |  | ['exa_json_path=$.client_ip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?'] |
| added_regex_field | src_port |  | ['exa_json_path=$.client_ip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?'] |
| added_attribute | ExtractionType |  | json |