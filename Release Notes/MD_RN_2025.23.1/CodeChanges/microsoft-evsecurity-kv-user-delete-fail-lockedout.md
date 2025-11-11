# Code Changes for microsoft-evsecurity-kv-user-delete-fail-lockedout (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'domain', 'event_code', 'event_id', 'event_name', 'host', 'login_id', 'result', 'src_domain', 'src_host', 'src_user', 'time', 'user', 'user_sid'] |
| edit_regex_field | src_domain |  | ['Subject=.*?Account Domain=({domain}({src_domain}[^;\"\s]+))'] |
| added_regex_field | domain |  | ['Subject=.*?Account Domain=({domain}({src_domain}[^;\"\s]+))'] |
| removed_attribute | DupFields |  | N/A |