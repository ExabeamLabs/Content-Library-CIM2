# Code Changes for microsoft-evsecurity-cef-endpoint-login-fail-4625-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['auth_package', 'auth_process', 'dest_domain', 'dest_host', 'dest_user', 'domain', 'event_code', 'event_id', 'event_name', 'failure_code', 'failure_reason', 'host', 'login_id', 'login_type', 'result', 'result_code', 'src_host', 'src_host_windows', 'src_ip', 'src_port', 'time', 'user', 'user_sid'] |
| edit_regex_field | domain |  | ['"targetDomainName":"({dest_domain}({domain}[^"\s]+?))\s*"'] |
| edit_regex_field | host |  | ['"computer":"({dest_host}({host}[\w\-.]+))'] |
| edit_regex_field | result_code |  | ['"status":"({failure_code}({result_code}[^"]+?))\s*"', '"subStatus":"({failure_code}({result_code}[^"]+?))\s*"'] |
| edit_regex_field | src_host_windows |  | ['"workstationName":"({src_host_windows}({src_host}[\w\-\.]+?))\s*"'] |
| edit_regex_field | user |  | ['"targetUserName":"({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*"'] |
| added_regex_field | dest_domain |  | ['"targetDomainName":"({dest_domain}({domain}[^"\s]+?))\s*"'] |
| added_regex_field | dest_host |  | ['"computer":"({dest_host}({host}[\w\-.]+))'] |
| added_regex_field | dest_user |  | ['"targetUserName":"({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*"'] |
| added_regex_field | failure_code |  | ['"status":"({failure_code}({result_code}[^"]+?))\s*"', '"subStatus":"({failure_code}({result_code}[^"]+?))\s*"'] |
| added_regex_field | src_host |  | ['"workstationName":"({src_host_windows}({src_host}[\w\-\.]+?))\s*"'] |
| removed_attribute | DupFields |  | N/A |