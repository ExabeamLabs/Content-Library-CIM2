# Code Changes for microsoft-evsecurity-json-user-delete-fail-instanceid (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['domain', 'event_code', 'event_name', 'host', 'login_id', 'src_domain', 'src_host', 'src_user', 'time', 'user', 'user_sid'] |
| edit_regex_field | src_domain |  | ['"5":"({domain}({src_domain}[^\"]*))'] |
| added_regex_field | domain |  | ['"5":"({domain}({src_domain}[^\"]*))'] |
| removed_attribute | DupFields |  | N/A |