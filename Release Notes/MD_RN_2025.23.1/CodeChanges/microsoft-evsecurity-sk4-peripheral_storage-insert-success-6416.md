# Code Changes for microsoft-evsecurity-sk4-peripheral_storage-insert-success-6416 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['device_pid', 'device_vid', 'domain', 'event_code', 'event_name', 'host', 'log_source', 'login_id', 'src_domain', 'src_ip', 'src_port', 'src_user', 'time', 'user', 'user_sid'] |
| edit_regex_field | domain |  | ['"SubjectDomainName":"(-|({src_domain}({domain}[^"]+)))'] |
| edit_regex_field | user |  | ['"SubjectUserName":"(-|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))"'] |
| added_regex_field | src_domain |  | ['"SubjectDomainName":"(-|({src_domain}({domain}[^"]+)))'] |
| added_regex_field | src_user |  | ['"SubjectUserName":"(-|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))"'] |
| removed_attribute | DupFields |  | N/A |