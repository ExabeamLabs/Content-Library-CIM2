# Code Changes for microsoft-evsecurity-mix-user-delete-success-4726 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_name', 'dest_domain', 'dest_user', 'dest_user_sid', 'domain', 'event_code', 'event_id', 'event_name', 'host', 'login_id', 'time', 'user', 'user_sid'] |
| edit_regex_field | dest_domain |  | ['Target Account.+?Account Name:\s*((?-i)\\+[rnt])*({account_name}({dest_user}[^:].+?))((?-i)\\+[rnt])*\s*(\\n|\\r\s\\t)?\s*Account Domain:\s*((?-i)\\+[rnt])*({dest_domain}[^:].+?)\s*(\\n\\n|\\r\s\\r\s\\n)?Additional Information:'] |
| edit_regex_field | dest_user |  | ['Target Account.+?Account Name:\s*((?-i)\\+[rnt])*({account_name}({dest_user}[^:].+?))((?-i)\\+[rnt])*\s*(\\n|\\r\s\\t)?\s*Account Domain:\s*((?-i)\\+[rnt])*({dest_domain}[^:].+?)\s*(\\n\\n|\\r\s\\r\s\\n)?Additional Information:'] |
| added_regex_field | account_name |  | ['Target Account.+?Account Name:\s*((?-i)\\+[rnt])*({account_name}({dest_user}[^:].+?))((?-i)\\+[rnt])*\s*(\\n|\\r\s\\t)?\s*Account Domain:\s*((?-i)\\+[rnt])*({dest_domain}[^:].+?)\s*(\\n\\n|\\r\s\\r\s\\n)?Additional Information:'] |
| removed_attribute | DupFields |  | N/A |