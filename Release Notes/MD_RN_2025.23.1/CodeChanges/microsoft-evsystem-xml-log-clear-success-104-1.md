# Code Changes for microsoft-evsystem-xml-log-clear-success-104-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['alert_severity', 'channel', 'channel_name', 'dest_host', 'dest_ip', 'dest_port', 'domain', 'event_code', 'event_name', 'host', 'process_id', 'result', 'run_level', 'src_domain', 'src_user', 'thread_id', 'time', 'user', 'user_sid'] |
| edit_regex_field | domain |  | ['<SubjectDomainName>(NT AUTHORITY|({src_domain}({domain}[^<]+)))'] |
| edit_regex_field | user |  | ['<SubjectUserName>(SYSTEM|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))'] |
| added_regex_field | src_domain |  | ['<SubjectDomainName>(NT AUTHORITY|({src_domain}({domain}[^<]+)))'] |
| added_regex_field | src_user |  | ['<SubjectUserName>(SYSTEM|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))'] |
| removed_attribute | DupFields |  | N/A |