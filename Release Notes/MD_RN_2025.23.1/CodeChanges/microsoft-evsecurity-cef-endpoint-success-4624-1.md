# Code Changes for microsoft-evsecurity-cef-endpoint-success-4624-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['auth_package', 'auth_process', 'dest_host', 'domain', 'event_code', 'event_id', 'event_name', 'host', 'login_id', 'login_type', 'process_dir', 'process_name', 'process_path', 'result', 'src_domain', 'src_host_windows', 'src_ip', 'src_port', 'src_user', 'time', 'user', 'user_sid'] |
| edit_regex_field | domain |  | ['"subjectDomainName":"({src_domain}({domain}[^"\s]+?))\s*"'] |
| edit_regex_field | host |  | ['"computer":"({dest_host}({host}[\w\-.]+))'] |
| edit_regex_field | user |  | ['"subjectUserName":"({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*"'] |
| added_regex_field | dest_host |  | ['"computer":"({dest_host}({host}[\w\-.]+))'] |
| added_regex_field | src_domain |  | ['"subjectDomainName":"({src_domain}({domain}[^"\s]+?))\s*"'] |
| added_regex_field | src_user |  | ['"subjectUserName":"({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*"'] |
| removed_attribute | DupFields |  | N/A |