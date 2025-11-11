# Code Changes for microsoft-evsecurity-kv-user-delete-fail-4743 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_name', 'dest_domain', 'dest_user', 'dest_user_sid', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'privileges', 'result', 'time', 'user', 'user_sid'] |
| edit_regex_field | dest_user |  | ['Target Computer:.+?Account Name:\s+({account_name}({dest_user}[^:]+?))\s+Account Domain:'] |
| added_regex_field | account_name |  | ['Target Computer:.+?Account Name:\s+({account_name}({dest_user}[^:]+?))\s+Account Domain:'] |
| removed_attribute | DupFields |  | N/A |