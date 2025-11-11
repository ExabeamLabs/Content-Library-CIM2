# Code Changes for microsoft-evsecurity-json-user-create-success-4720 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_domain', 'account_id', 'account_name', 'dest_domain', 'dest_user', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'src_domain', 'src_user', 'time', 'user'] |
| edit_regex_field | account_domain |  | ['"TargetDomainName":"({dest_domain}({account_domain}[^"]+))'] |
| edit_regex_field | account_name |  | ['"TargetUserName":"({dest_user}({account_name}[^"]+))'] |
| edit_regex_field | domain |  | ['"SubjectDomainName":"({src_domain}({domain}[^"]+))'] |
| edit_regex_field | user |  | ['"SubjectUserName":"({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| added_regex_field | dest_domain |  | ['"TargetDomainName":"({dest_domain}({account_domain}[^"]+))'] |
| added_regex_field | dest_user |  | ['"TargetUserName":"({dest_user}({account_name}[^"]+))'] |
| added_regex_field | src_domain |  | ['"SubjectDomainName":"({src_domain}({domain}[^"]+))'] |
| added_regex_field | src_user |  | ['"SubjectUserName":"({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| removed_attribute | DupFields |  | N/A |