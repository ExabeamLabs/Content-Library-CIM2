# Code Changes for microsoft-evsecurity-cef-endpoint-4768 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_domain', 'dest_user', 'dest_user_sid', 'domain', 'event_code', 'event_id', 'event_name', 'failure_code', 'host', 'result', 'result_code', 'service_name', 'src_ip', 'src_port', 'ticket_encryption_type', 'ticket_options', 'time', 'user', 'user_sid'] |
| edit_regex_field | domain |  | ['"targetDomainName":"({dest_domain}({domain}[^"\s]+?))\s*"'] |
| edit_regex_field | result_code |  | ['"status":"({failure_code}({result_code}[^"]+?))\s*"'] |
| edit_regex_field | user |  | ['"targetUserName":"({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*"'] |
| edit_regex_field | user_sid |  | ['"targetSid":"({dest_user_sid}({user_sid}[^"\s]+?))\s*"'] |
| added_regex_field | dest_domain |  | ['"targetDomainName":"({dest_domain}({domain}[^"\s]+?))\s*"'] |
| added_regex_field | dest_user |  | ['"targetUserName":"({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*"'] |
| added_regex_field | dest_user_sid |  | ['"targetSid":"({dest_user_sid}({user_sid}[^"\s]+?))\s*"'] |
| added_regex_field | failure_code |  | ['"status":"({failure_code}({result_code}[^"]+?))\s*"'] |
| removed_attribute | DupFields |  | N/A |