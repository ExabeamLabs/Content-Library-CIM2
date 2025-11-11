# Code Changes for microsoft-evsecurity-kv-user-delete-fail-644 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['domain', 'event_code', 'event_id', 'login_id', 'src_domain', 'src_host', 'src_user', 'user', 'user_sid'] |
| edit_regex_field | src_domain |  | ['CallerDomain=\"+({domain}({src_domain}[^\"]+))\"'] |
| added_regex_field | domain |  | ['CallerDomain=\"+({domain}({src_domain}[^\"]+))\"'] |
| removed_attribute | DupFields |  | N/A |