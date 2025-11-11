# Code Changes for microsoft-evsecurity-json-endpoint-login-fail-4625-4 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['auth_package', 'auth_process', 'dest_domain', 'dest_host', 'dest_user', 'domain', 'event_code', 'event_name', 'failure_code', 'host', 'key_length', 'login_type', 'result_code', 'src_domain', 'src_host', 'src_host_windows', 'src_ip', 'src_port', 'src_user', 'subject_sid', 'time', 'user', 'user_sid', 'user_upn'] |
| edit_regex_field | domain |  | ['"TargetDomainName\\*":\\*"({dest_domain}({domain}[^."\\]+))'] |
| edit_regex_field | host |  | ['"(Hostname|MachineName)\\*":\\*"({dest_host}({host}[\w\-.]*))'] |
| edit_regex_field | result_code |  | ['"SubStatus\\*":\\*"({failure_code}({result_code}[^"\\]+))'] |
| edit_regex_field | src_host_windows |  | ['"WorkstationName\\*":\\*"({src_host_windows}({src_host}[\w\-\.]+))'] |
| edit_regex_field | user |  | ['"TargetUserName\\?":\\?"\s*(({user_upn}([A-Za-z0-9]+[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+(\.[^\'\]\s"\\,\|]+)?)|({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))'] |
| edit_regex_field | user_upn |  | ['"TargetUserName\\?":\\?"\s*(({user_upn}([A-Za-z0-9]+[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+(\.[^\'\]\s"\\,\|]+)?)|({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))'] |
| added_regex_field | dest_domain |  | ['"TargetDomainName\\*":\\*"({dest_domain}({domain}[^."\\]+))'] |
| added_regex_field | dest_host |  | ['"(Hostname|MachineName)\\*":\\*"({dest_host}({host}[\w\-.]*))'] |
| added_regex_field | dest_user |  | ['"TargetUserName\\?":\\?"\s*(({user_upn}([A-Za-z0-9]+[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+(\.[^\'\]\s"\\,\|]+)?)|({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))'] |
| added_regex_field | failure_code |  | ['"SubStatus\\*":\\*"({failure_code}({result_code}[^"\\]+))'] |
| added_regex_field | src_host |  | ['"WorkstationName\\*":\\*"({src_host_windows}({src_host}[\w\-\.]+))'] |
| removed_attribute | DupFields |  | N/A |