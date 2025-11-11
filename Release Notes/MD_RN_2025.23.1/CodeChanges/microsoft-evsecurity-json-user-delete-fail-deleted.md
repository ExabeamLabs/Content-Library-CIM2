# Code Changes for microsoft-evsecurity-json-user-delete-fail-deleted (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_name', 'dest_host', 'dest_ip', 'dest_port', 'dest_user', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'src_ip', 'src_port', 'time', 'user', 'user_sid'] |
| edit_regex_field | dest_user |  | ['"UserIDDst":"({account_name}({dest_user}[^\"]+))'] |
| edit_regex_field | host |  | ['"HostID":"({dest_host}({host}[\w\-.]+))'] |
| added_regex_field | account_name |  | ['"UserIDDst":"({account_name}({dest_user}[^\"]+))'] |
| added_regex_field | dest_host |  | ['"HostID":"({dest_host}({host}[\w\-.]+))'] |
| removed_attribute | DupFields |  | N/A |