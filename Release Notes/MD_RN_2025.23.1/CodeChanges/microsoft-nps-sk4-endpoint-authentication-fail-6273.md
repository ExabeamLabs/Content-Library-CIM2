# Code Changes for microsoft-nps-sk4-endpoint-authentication-fail-6273 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['auth_server', 'dest_ip', 'dest_port', 'domain', 'email_address', 'email_domain', 'event_code', 'event_name', 'failure_reason', 'host', 'location', 'log_source', 'login_id', 'src_domain', 'src_host', 'src_ip', 'src_port', 'src_user', 'time', 'user', 'user_sid', 'user_type'] |
| edit_regex_field | domain |  | ['"SubjectDomainName":"(-|({src_domain}({domain}[^"]+)))', '"SubjectUserName":"((?:host\/)({src_host}[^"]+)|({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|(({domain}[^\\"]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))"'] |
| edit_regex_field | user |  | ['"SubjectUserName":"((?:host\/)({src_host}[^"]+)|({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|(({domain}[^\\"]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))"', '"SubjectUserName":"(-|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))"'] |
| added_regex_field | src_domain |  | ['"SubjectDomainName":"(-|({src_domain}({domain}[^"]+)))'] |
| added_regex_field | src_user |  | ['"SubjectUserName":"(-|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))"'] |
| removed_attribute | DupFields |  | N/A |