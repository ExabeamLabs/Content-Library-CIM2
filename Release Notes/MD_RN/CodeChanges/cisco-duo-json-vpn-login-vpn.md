# Code Changes for cisco-duo-json-vpn-login-vpn (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A | ['browser', 'browser_version', 'email_address', 'email_domain', 'event_name', 'factor', 'failure_reason', 'host', 'mfa_device', 'os', 'os_version', 'result', 'service_name', 'src_country', 'src_ip', 'time', 'user'] | ['browser', 'browser_version', 'domain', 'email_address', 'email_domain', 'event_name', 'factor', 'failure_reason', 'host', 'mfa_device', 'os', 'os_version', 'result', 'service_name', 'src_country', 'src_ip', 'time', 'user'] |
| edit_regex_field | user | ['"user":[^\}]+?"name":"({user}[\w\.\-\!\#\^\~]{1,40}\$?)"'] | ['"user":[^\}]*"name":"(({domain}[^\\]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)"'] |
| added_regex_field | domain | [] | ['"user":[^\}]*"name":"(({domain}[^\\]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)"'] |