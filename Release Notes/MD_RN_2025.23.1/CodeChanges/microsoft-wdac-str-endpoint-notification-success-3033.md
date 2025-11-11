# Code Changes for microsoft-wdac-str-endpoint-notification-success-3033 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_id', 'dest_host', 'event_code', 'host', 'process_dir', 'process_name', 'process_path', 'time', 'user'] |
| edit_regex_field | host |  | ['\s({dest_host}({host}[\w\-.]+))\s+MSWinEventLog'] |
| added_regex_field | dest_host |  | ['\s({dest_host}({host}[\w\-.]+))\s+MSWinEventLog'] |
| removed_attribute | DupFields |  | N/A |