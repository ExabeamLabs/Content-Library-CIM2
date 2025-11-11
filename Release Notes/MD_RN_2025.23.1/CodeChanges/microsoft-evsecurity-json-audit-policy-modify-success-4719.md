# Code Changes for microsoft-evsecurity-json-audit-policy-modify-success-4719 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['audit_category', 'audit_policy_name', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'src_domain', 'src_user', 'sub_category', 'time', 'user'] |
| edit_regex_field | domain |  | ['"SubjectDomainName"+:"+({src_domain}({domain}[^"]+))'] |
| edit_regex_field | user |  | ['"SubjectUserName"+:"+({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| added_regex_field | src_domain |  | ['"SubjectDomainName"+:"+({src_domain}({domain}[^"]+))'] |
| added_regex_field | src_user |  | ['"SubjectUserName"+:"+({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| removed_attribute | DupFields |  | N/A |