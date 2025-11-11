# Code Changes for microsoft-evsecurity-xml-group-list-4798 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_domain', 'dest_login_id', 'dest_user', 'dest_user_sid', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'login_type', 'process_dir', 'process_id', 'process_name', 'process_path', 'result', 'run_level', 'src_domain', 'src_port', 'src_user', 'time', 'user', 'user_sid'] |
| edit_regex_field | domain |  | ['<Data Name\\=(\'|")SubjectDomainName(\'|")>(-|({src_domain}({domain}[^<>]+)))<'] |
| edit_regex_field | user |  | ['<Data Name\\=(\'|")SubjectUserName(\'|")>(-|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))<'] |
| added_regex_field | src_domain |  | ['<Data Name\\=(\'|")SubjectDomainName(\'|")>(-|({src_domain}({domain}[^<>]+)))<'] |
| added_regex_field | src_user |  | ['<Data Name\\=(\'|")SubjectUserName(\'|")>(-|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))<'] |
| removed_attribute | DupFields |  | N/A |