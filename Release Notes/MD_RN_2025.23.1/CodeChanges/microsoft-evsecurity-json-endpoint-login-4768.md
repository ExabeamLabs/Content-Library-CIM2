# Code Changes for microsoft-evsecurity-json-endpoint-login-4768 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'auth_type', 'dest_domain', 'dest_user', 'domain', 'event_code', 'event_name', 'host', 'result_code', 'service_name', 'src_ip', 'src_port', 'ticket_encryption_type', 'ticket_options', 'time', 'user', 'user_sid', 'user_upn'] |
| edit_regex_field | domain |  | ['"(TargetDomainName|SuppliedRealmName)":"({dest_domain}({domain}[^."]+))'] |
| edit_regex_field | user |  | ['"(TargetUserName|AccountName)":"\s*(({user_upn}([A-Za-z0-9]+[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+(\.[^\]\s"\\,\|]+)?)|({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))', 'exa_json_path=$.TargetUserName,exa_regex=\s*(({user_upn}([A-Za-z0-9]+[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+(\.[^\]\s"\\,\|]+)?)|({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))'] |
| edit_regex_field | user_upn |  | ['"(TargetUserName|AccountName)":"\s*(({user_upn}([A-Za-z0-9]+[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+(\.[^\]\s"\\,\|]+)?)|({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))', 'exa_json_path=$.TargetUserName,exa_regex=\s*(({user_upn}([A-Za-z0-9]+[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+(\.[^\]\s"\\,\|]+)?)|({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))'] |
| added_regex_field | dest_domain |  | ['"(TargetDomainName|SuppliedRealmName)":"({dest_domain}({domain}[^."]+))'] |
| added_regex_field | dest_user |  | ['"(TargetUserName|AccountName)":"\s*(({user_upn}([A-Za-z0-9]+[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+(\.[^\]\s"\\,\|]+)?)|({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))', 'exa_json_path=$.TargetUserName,exa_regex=\s*(({user_upn}([A-Za-z0-9]+[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+(\.[^\]\s"\\,\|]+)?)|({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))'] |
| removed_attribute | DupFields |  | N/A |