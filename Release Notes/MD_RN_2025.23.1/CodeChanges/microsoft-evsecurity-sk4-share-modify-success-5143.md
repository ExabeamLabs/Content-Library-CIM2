# Code Changes for microsoft-evsecurity-sk4-share-modify-success-5143 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'share_name', 'share_path', 'time', 'user', 'user_sid'] |
| edit_regex_field | host |  | ['"Computer":"({dest_host}({host}[\w\-.]+))'] |
| added_regex_field | dest_host |  | ['"Computer":"({dest_host}({host}[\w\-.]+))'] |
| removed_attribute | DupFields |  | N/A |