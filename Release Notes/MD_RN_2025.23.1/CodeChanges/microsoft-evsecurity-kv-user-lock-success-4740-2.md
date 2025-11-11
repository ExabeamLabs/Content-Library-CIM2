# Code Changes for microsoft-evsecurity-kv-user-lock-success-4740-2 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_user', 'dest_user_sid', 'domain', 'event_code', 'event_id', 'host', 'login_id', 'process_guid', 'src_domain', 'src_user', 'user', 'user_sid'] |
| edit_regex_field | domain |  | ['SubjectDomainName="({domain}[^"]+)"', 'TargetDomainName="({domain}({src_domain}[^"]+))"', 'TargetDomainName="({domain}[^"]+)"'] |
| edit_regex_field | src_domain |  | ['SubjectDomainName="({src_domain}[^"]+)"', 'TargetDomainName="({domain}({src_domain}[^"]+))"'] |
| edit_regex_field | user |  | ['SubjectUserName="({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))"', 'TargetUserName="({user}[\w\.\-]{1,40}\$?)"'] |
| added_regex_field | src_user |  | ['SubjectUserName="({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))"', 'SubjectUserName="({src_user}[\w\.\-\!\#\^\~]{1,40}\$?)"'] |
| removed_attribute | DupFields |  | N/A |