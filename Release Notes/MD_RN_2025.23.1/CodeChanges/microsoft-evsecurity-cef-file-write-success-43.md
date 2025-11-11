# Code Changes for microsoft-evsecurity-cef-file-write-success-43 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'access_mask', 'dest_host', 'domain', 'event_code', 'event_name', 'file_dir', 'file_ext', 'file_name', 'file_path', 'host', 'login_id', 'time', 'user', 'user_sid'] |
| edit_regex_field | host |  | ['shost=({dest_host}({host}[^\s]+))'] |
| added_regex_field | dest_host |  | ['shost=({dest_host}({host}[^\s]+))'] |
| removed_attribute | DupFields |  | N/A |