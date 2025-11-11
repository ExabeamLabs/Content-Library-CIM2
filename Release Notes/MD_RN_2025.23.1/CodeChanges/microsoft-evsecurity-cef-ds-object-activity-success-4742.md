# Code Changes for microsoft-evsecurity-cef-ds-object-activity-success-4742 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'dest_user', 'domain', 'ds_object_dn', 'event_code', 'event_id', 'event_name', 'host', 'login_id', 'new_value', 'object_name', 'old_value', 'result', 'src_domain', 'src_user', 'time', 'uac_status', 'user', 'user_sid'] |
| edit_regex_field | domain |  | ['"subjectDomainName":"({src_domain}({domain}[^"\s]+?))\s*"'] |
| edit_regex_field | host |  | ['"computer":"({dest_host}({host}[\w\-.]+))'] |
| edit_regex_field | user |  | ['"subjectUserName":"({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*"'] |
| added_regex_field | dest_host |  | ['"computer":"({dest_host}({host}[\w\-.]+))'] |
| added_regex_field | src_domain |  | ['"subjectDomainName":"({src_domain}({domain}[^"\s]+?))\s*"'] |
| added_regex_field | src_user |  | ['"subjectUserName":"({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*"'] |
| removed_attribute | DupFields |  | N/A |