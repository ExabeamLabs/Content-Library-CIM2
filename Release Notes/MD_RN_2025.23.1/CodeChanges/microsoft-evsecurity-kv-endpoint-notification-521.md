# Code Changes for microsoft-evsecurity-kv-endpoint-notification-521 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['domain', 'event_code', 'event_name', 'host', 'login_id', 'process_dir', 'process_id', 'process_name', 'process_path', 'result', 'result_code', 'run_level', 'severity', 'src_domain', 'src_user', 'time', 'transaction_id', 'user', 'user_sid'] |
| edit_regex_field | domain |  | ['"Domain"*:"*(-|({src_domain}({domain}[^"]+)))', '"SubjectDomainName"*:"*(-|(){src_domain}({domain}[^"]+)))"'] |
| edit_regex_field | user |  | ['"AccountName"*:"*({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))"', '"SubjectUserName"*:"*({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))"'] |
| added_regex_field | src_domain |  | ['"Domain"*:"*(-|({src_domain}({domain}[^"]+)))', '"SubjectDomainName"*:"*(-|(){src_domain}({domain}[^"]+)))"'] |
| added_regex_field | src_user |  | ['"AccountName"*:"*({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))"', '"SubjectUserName"*:"*({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))"'] |
| removed_attribute | DupFields |  | N/A |