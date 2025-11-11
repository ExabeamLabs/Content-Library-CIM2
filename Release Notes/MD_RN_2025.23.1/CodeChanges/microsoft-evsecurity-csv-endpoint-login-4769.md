# Code Changes for microsoft-evsecurity-csv-endpoint-login-4769 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_domain', 'dest_user', 'domain', 'event_code', 'host', 'result', 'result_code', 'src_host', 'src_ip', 'src_port', 'ticket_encryption_type', 'ticket_options', 'time', 'user'] |
| edit_regex_field | domain |  | ['TargetDomainName:({dest_domain}({domain}[^,]+)),', 'TargetUserName:({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))@({dest_domain}({domain}[^,]+)),'] |
| edit_regex_field | user |  | ['TargetUserName:({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))@({dest_domain}({domain}[^,]+)),'] |
| added_regex_field | dest_domain |  | ['TargetDomainName:({dest_domain}({domain}[^,]+)),', 'TargetUserName:({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))@({dest_domain}({domain}[^,]+)),'] |
| added_regex_field | dest_user |  | ['TargetUserName:({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))@({dest_domain}({domain}[^,]+)),'] |
| removed_attribute | DupFields |  | N/A |