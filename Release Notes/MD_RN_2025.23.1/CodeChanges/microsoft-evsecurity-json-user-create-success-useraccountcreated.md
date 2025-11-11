# Code Changes for microsoft-evsecurity-json-user-create-success-useraccountcreated (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_name', 'additional_info', 'dest_ip', 'dest_port', 'dest_user', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'src_ip', 'src_port', 'time', 'user', 'user_sid', 'user_type'] |
| edit_regex_field | account_name |  | ['"UserIDDst":"({dest_user}({account_name}[^"]+))'] |
| added_regex_field | dest_user |  | ['"UserIDDst":"({dest_user}({account_name}[^"]+))'] |
| removed_attribute | DupFields |  | N/A |