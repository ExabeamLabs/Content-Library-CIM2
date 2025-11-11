# Code Changes for microsoft-evsecurity-kv-driver-load-fail-5038 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'event_code', 'event_name', 'file_dir', 'file_ext', 'file_name', 'file_path', 'host', 'time'] |
| edit_regex_field | host |  | [':\d+\s({dest_host}({host}[^\s]+))\sMSWinEventLog'] |
| added_regex_field | dest_host |  | [':\d+\s({dest_host}({host}[^\s]+))\sMSWinEventLog'] |
| removed_attribute | DupFields |  | N/A |