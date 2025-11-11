# Code Changes for microsoft-evsecurity-json-audit-policy-modify-4907 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['audit_policy_name', 'domain', 'event_code', 'event_name', 'handle_id', 'host', 'login_id', 'object', 'object_server', 'object_type', 'process_dir', 'process_id', 'process_name', 'process_path', 'src_domain', 'src_user', 'time', 'user', 'user_sid'] |
| edit_regex_field | domain |  | ['"SubjectDomainName"+:"+({src_domain}({domain}[^"]+))'] |
| edit_regex_field | user |  | ['"SubjectUserName"+:"+({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| added_regex_field | src_domain |  | ['"SubjectDomainName"+:"+({src_domain}({domain}[^"]+))'] |
| added_regex_field | src_user |  | ['"SubjectUserName"+:"+({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| removed_attribute | DupFields |  | N/A |