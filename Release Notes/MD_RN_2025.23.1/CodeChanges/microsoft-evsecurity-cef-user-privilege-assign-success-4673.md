# Code Changes for microsoft-evsecurity-cef-user-privilege-assign-success-4673 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'object_server', 'privileges', 'result', 'time', 'user'] |
| edit_regex_field | host |  | ['\sdhost=({dest_host}({host}[\w\-.]+?))(\s+[^\s]+=|\s*$)'] |
| added_regex_field | dest_host |  | ['\sdhost=({dest_host}({host}[\w\-.]+?))(\s+[^\s]+=|\s*$)'] |
| removed_attribute | DupFields |  | N/A |