# Code Changes for microsoft-evsecurity-json-user-switch-success-4648-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'dest_ip', 'dest_port', 'dest_user', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'process_id', 'process_name', 'src_ip', 'src_port', 'time', 'user', 'user_sid'] |
| edit_regex_field | dest_user |  | ['"UserIDDst":"({account}({dest_user}[^"]+))'] |
| added_regex_field | account |  | ['"UserIDDst":"({account}({dest_user}[^"]+))'] |
| removed_attribute | DupFields |  | N/A |