# Code Changes for microsoft-evsecurity-kv-user-create-success-4720 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_domain', 'account_id', 'account_name', 'dest_domain', 'dest_user', 'domain', 'event_code', 'event_id', 'host', 'login_id', 'src_host', 'time', 'user', 'user_sid'] |
| edit_regex_field | account_domain |  | ['ACCOUNT_DOMAIN\s*=\s*({dest_domain}({account_domain}[^\s]+))'] |
| edit_regex_field | account_name |  | ['ACCOUNT_NAME\s*=\s*({dest_user}({account_name}[^\s]+))'] |
| added_regex_field | dest_domain |  | ['ACCOUNT_DOMAIN\s*=\s*({dest_domain}({account_domain}[^\s]+))'] |
| added_regex_field | dest_user |  | ['ACCOUNT_NAME\s*=\s*({dest_user}({account_name}[^\s]+))'] |
| removed_attribute | DupFields |  | N/A |