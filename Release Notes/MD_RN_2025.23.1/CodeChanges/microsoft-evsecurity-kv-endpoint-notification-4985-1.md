# Code Changes for microsoft-evsecurity-kv-endpoint-notification-4985-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'process_dir', 'process_id', 'process_name', 'process_path', 'src_domain', 'src_ip', 'src_port', 'src_user', 'time', 'user', 'user_sid'] |
| edit_regex_field | domain |  | ['SubjectDomainName="+({src_domain}({domain}[^"]+))'] |
| edit_regex_field | host |  | ['({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\+\d+:\d+)\s({host}[^\s]+)', 'Computer="+({dest_host}({host}[^"]+))'] |
| edit_regex_field | user |  | ['SubjectUserName="+({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| added_regex_field | dest_host |  | ['Computer="+({dest_host}({host}[^"]+))'] |
| added_regex_field | src_domain |  | ['SubjectDomainName="+({src_domain}({domain}[^"]+))'] |
| added_regex_field | src_user |  | ['SubjectUserName="+({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| removed_attribute | DupFields |  | N/A |