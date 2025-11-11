# Code Changes for microsoft-evsecurity-kv-user-delete-fail-accountname (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'result', 'src_host', 'time', 'user', 'user_id', 'user_sid'] |
| edit_regex_field | host |  | ['\sComputerName=({dest_host}({host}[\w\-.]+))'] |
| added_regex_field | dest_host |  | ['\sComputerName=({dest_host}({host}[\w\-.]+))'] |
| removed_attribute | DupFields |  | N/A |