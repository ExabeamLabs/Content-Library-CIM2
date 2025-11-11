# Code Changes for microsoft-evsecurity-kv-user-lock-success-4740-3 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['domain', 'event_code', 'event_name', 'host', 'login_id', 'src_domain', 'src_host', 'src_user', 'time', 'user', 'user_sid'] |
| edit_regex_field | src_domain |  | ['Subject:Account Domain=({domain}({src_domain}[^\s]+))'] |
| added_regex_field | domain |  | ['Subject:Account Domain=({domain}({src_domain}[^\s]+))'] |
| removed_attribute | DupFields |  | N/A |