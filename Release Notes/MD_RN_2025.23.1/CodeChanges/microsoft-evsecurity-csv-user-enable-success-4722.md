# Code Changes for microsoft-evsecurity-csv-user-enable-success-4722 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_domain', 'dest_host', 'dest_user', 'domain', 'event_code', 'host', 'login_id', 'time', 'user'] |
| edit_regex_field | host |  | ['({host}({dest_host}[\w.\-]+)),ユーザー アカウントが有効化されました。'] |
| added_regex_field | dest_host |  | ['({host}({dest_host}[\w.\-]+)),ユーザー アカウントが有効化されました。'] |
| removed_attribute | DupFields |  | N/A |