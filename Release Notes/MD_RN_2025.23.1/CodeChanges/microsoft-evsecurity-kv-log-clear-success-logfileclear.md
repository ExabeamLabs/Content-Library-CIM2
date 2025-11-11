# Code Changes for microsoft-evsecurity-kv-log-clear-success-logfileclear (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'dest_ip', 'dest_port', 'domain', 'event_code', 'event_name', 'host', 'log_name', 'login_id', 'process_id', 'src_domain', 'src_user', 'thread_id', 'time', 'user', 'user_sid'] |
| edit_regex_field | domain |  | ['<SubjectDomainName>({src_domain}({domain}[^<]+))'] |
| edit_regex_field | user |  | ['<SubjectUserName>({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| added_regex_field | src_domain |  | ['<SubjectDomainName>({src_domain}({domain}[^<]+))'] |
| added_regex_field | src_user |  | ['<SubjectUserName>({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| removed_attribute | DupFields |  | N/A |