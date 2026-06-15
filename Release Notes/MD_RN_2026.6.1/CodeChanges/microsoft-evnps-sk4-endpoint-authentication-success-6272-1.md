# Code Changes for microsoft-evnps-sk4-endpoint-authentication-success-6272-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | domain |  | ['"SubjectDomainName":"(-|({src_domain}({domain}[^"]+)))', '"SubjectUserName":"((?:host\/)({src_host}[^"]+)|({user_upn}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|(({=domain}[^\\"]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))"'] |
| edit_regex_field | src_host |  | ['"SubjectUserName":"((?:host\/)({src_host}[^"]+)|({user_upn}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|(({=domain}[^\\"]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))"'] |
| edit_regex_field | user |  | ['"SubjectUserName":"((?:host\/)({src_host}[^"]+)|({user_upn}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|(({=domain}[^\\"]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))"', '"SubjectUserName":"(-|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))"'] |
| edit_regex_field | user_upn |  | ['"SubjectUserName":"((?:host\/)({src_host}[^"]+)|({user_upn}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|(({=domain}[^\\"]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))"'] |