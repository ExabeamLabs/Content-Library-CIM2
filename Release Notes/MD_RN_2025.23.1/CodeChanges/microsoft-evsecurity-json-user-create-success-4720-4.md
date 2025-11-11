# Code Changes for microsoft-evsecurity-json-user-create-success-4720-4 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_domain', 'account_id', 'account_name', 'dest_domain', 'dest_user', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'time', 'user'] |
| edit_regex_field | account_domain |  | ['"1":"({dest_domain}({account_domain}[^"]+))'] |
| edit_regex_field | account_name |  | ['"0":"({dest_user}({account_name}[^"]+))'] |
| added_regex_field | dest_domain |  | ['"1":"({dest_domain}({account_domain}[^"]+))'] |
| added_regex_field | dest_user |  | ['"0":"({dest_user}({account_name}[^"]+))'] |
| removed_attribute | DupFields |  | N/A |