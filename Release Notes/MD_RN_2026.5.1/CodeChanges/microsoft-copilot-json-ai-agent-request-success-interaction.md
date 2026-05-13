# Code Changes for microsoft-copilot-json-ai-agent-request-success-interaction (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| COULD_NOT_COMPARE | TimeFormat |  | ["yyyy-MM-dd'T'HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ssZ"] |
| changed_parsed_fields | N/A |  | ['access', 'app', 'app_type', 'email_address', 'email_domain', 'event_name', 'full_name', 'src_ip', 'src_port', 'time', 'url', 'user', 'user_id', 'user_type'] |
| edit_regex_field | email_address |  | ['"UserId"\s*:\s*"(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"', 'exa_json_path=$..UserId,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))'] |
| edit_regex_field | email_domain |  | ['"UserId"\s*:\s*"(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"', 'exa_json_path=$..UserId,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))'] |
| edit_regex_field | src_ip |  | ['"ClientIP"\s*:\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"', 'exa_json_path=$..ClientIP,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?'] |
| edit_regex_field | src_port |  | ['"ClientIP"\s*:\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"', 'exa_json_path=$..ClientIP,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?'] |
| added_regex_field | access |  | ['"Action"\s*:\s*"({access}[^",]+)"'] |
| added_regex_field | app |  | ['"AppHost"\s*:\s*"({app}[^",]+)"'] |
| added_regex_field | app_type |  | ['"AppIdentity"\s*:\s*"({app_type}[^",]+)"'] |
| added_regex_field | event_name |  | ['"Operation"\s*:\s*"({event_name}[^",]+)"'] |
| added_regex_field | full_name |  | ['"AccountDisplayName"\s*:\s*"({full_name}[^"]+)"'] |
| added_regex_field | time |  | ['"CreationTime"\s*:\s*({time}[^"]+)"'] |
| added_regex_field | url |  | ['"SiteUrl"\s*:\s*"({url}[^",]+)"'] |
| added_regex_field | user |  | ['"UserId"\s*:\s*"(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"'] |
| added_regex_field | user_id |  | ['"UserKey"\s*:\s*"({user_id}[\w\.\-\!\#\^\~]{1,40}\$?)"'] |
| added_regex_field | user_type |  | ['"UserType"\s*:\s*"?({user_type}\d+)'] |