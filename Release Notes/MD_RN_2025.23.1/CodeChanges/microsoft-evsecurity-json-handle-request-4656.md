# Code Changes for microsoft-evsecurity-json-handle-request-4656 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'dest_host', 'dest_ip', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'object', 'object_id', 'object_server', 'object_type', 'operation_type', 'privileges', 'process_dir', 'process_id', 'process_name', 'process_path', 'src_domain', 'src_user', 'time', 'transaction_id', 'user', 'user_sid'] |
| edit_regex_field | access |  | ['"AccessReason"+:"+(-|({privileges}({access}[^",]+)))', 'Accesses:(?:\s|\\t|\\r|\\n)*({privileges}({access}[^:]+?))(?:\s|\\t|\\r|\\n)*Access Reasons:'] |
| edit_regex_field | dest_host |  | ['"Hostname"+:"+({dest_host}({host}[^",]+))', '(?i)\w+\s*\d+\s*\d+:\d+:\d+\s+(::ffff:)?(({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|(am|pm|\d{4}|({dest_host}[\w\-.]+)))\s'] |
| edit_regex_field | domain |  | ['"SubjectDomainName"+:"+({src_domain}({domain}[^",]+))"'] |
| edit_regex_field | host |  | ['"Hostname"+:"+({dest_host}({host}[^",]+))'] |
| edit_regex_field | privileges |  | ['"AccessReason"+:"+(-|({privileges}({access}[^",]+)))', '"PrivilegeList"+:"+(-|({privileges}[^",]+))', 'Accesses:(?:\s|\\t|\\r|\\n)*({privileges}({access}[^:]+?))(?:\s|\\t|\\r|\\n)*Access Reasons:'] |
| edit_regex_field | user |  | ['"SubjectUserName"+:"+({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))"'] |
| added_regex_field | src_domain |  | ['"SubjectDomainName"+:"+({src_domain}({domain}[^",]+))"'] |
| added_regex_field | src_user |  | ['"SubjectUserName"+:"+({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))"'] |
| removed_attribute | DupFields |  | N/A |