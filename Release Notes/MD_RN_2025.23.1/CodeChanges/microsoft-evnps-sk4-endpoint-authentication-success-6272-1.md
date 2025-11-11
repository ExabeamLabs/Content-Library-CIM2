# Code Changes for microsoft-evnps-sk4-endpoint-authentication-success-6272-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['auth_server', 'auth_type', 'dest_ip', 'dest_port', 'domain', 'event_code', 'event_name', 'host', 'log_source', 'login_id', 'src_domain', 'src_host', 'src_ip', 'src_mac', 'src_port', 'src_user', 'time', 'user', 'user_sid', 'user_type', 'user_upn'] |
| edit_regex_field | domain |  | ['"SubjectDomainName":"(-|({src_domain}({domain}[^"]+)))', '"SubjectUserName":"((?:host\/)({src_host}[^"]+)|({user_upn}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|(({=domain}[^\\"]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))"'] |
| edit_regex_field | user |  | ['"SubjectUserName":"((?:host\/)({src_host}[^"]+)|({user_upn}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|(({=domain}[^\\"]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))"', '"SubjectUserName":"(-|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))"'] |
| added_regex_field | src_domain |  | ['"SubjectDomainName":"(-|({src_domain}({domain}[^"]+)))'] |
| added_regex_field | src_user |  | ['"SubjectUserName":"(-|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))"'] |
| removed_attribute | DupFields |  | N/A |