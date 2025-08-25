# Code Changes for slack-s-cef-file-success-action (Parser)

| Code Change | Field Name | 2025.13.1 | 2025.14.1 |
|-------------|------------|-----------|------------|
| COULD_NOT_COMPARE | TimeFormat | yyyy-MM-dd'T'HH:mm:ss.SSSZ | ["yyyy-MM-dd'T'HH:mm:ss.SSSZ", 'epoch_sec'] |
| changed_parsed_fields | N/A | ['app', 'domain', 'email_address', 'email_domain', 'full_name', 'object', 'operation', 'src_ip', 'src_port', 'time', 'user_id'] | ['app', 'domain', 'email_address', 'full_name', 'object', 'operation', 'src_ip', 'src_port', 'time', 'user_agent', 'user_id'] |
| edit_regex_field | app | ['\WdestinationServiceName=({app}Slack)'] | ['.?destinationServiceName=({app}(s|S)lack)', 'exa_regex=destinationServiceName=({app}Slack)'] |
| edit_regex_field | email_address | ['"email":"(|({email_address}[^@]+@({email_domain}[^"]+?)))"'] | ['"email":"(|({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))"', 'exa_json_path=$.actor.user.email,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)'] |
| removed_regex_field | email_domain | ['"email":"(|({email_address}[^@]+@({email_domain}[^"]+?)))"'] | [] |
| edit_regex_field | full_name | ['user":\{"id":"({user_id}[^"]+)","name":"({full_name}[^"]+)"'] | ['"user":\{[^\}]*?"name":"({full_name}[^"]+)', 'user":\{"id":"({user_id}[^"]+)","name":"({full_name}[^"]+)"'] |
| edit_regex_field | object | ['"entity":\{"[^"]+":"[^"]+","[^"]+":\{("[^"]+":"[^"]+",){2}"name":"({object}[^"]+)"'] | ['"entity":.+?"name":"({object}[^"]+)"'] |
| edit_regex_field | src_ip | ['"ip_address":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"'] | ['"ip_address":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"', 'exa_json_path=$.context.ip_address,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?'] |
| edit_regex_field | src_port | ['"ip_address":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"'] | ['"ip_address":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"', 'exa_json_path=$.context.ip_address,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?'] |
| edit_regex_field | time | ['({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)\s+'] | ['"date_create":({time}\d{10})', '({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)\s+', 'exa_json_path=$.date_create,exa_regex=({time}\d{10})'] |
| edit_regex_field | user_id | ['user":\{"id":"({user_id}[^"]+)","name":"({full_name}[^"]+)"'] | ['"user":\{[^\}]*?"id":"({user_id}[^"]+)', 'user":\{"id":"({user_id}[^"]+)","name":"({full_name}[^"]+)"'] |
| added_regex_field | user_agent | [] | ['"ua":"({user_agent}[^"]+)"'] |
| added_attribute | ExtractionType | N/A | json |