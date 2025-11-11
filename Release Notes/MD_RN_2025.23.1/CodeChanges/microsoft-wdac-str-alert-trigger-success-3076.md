# Code Changes for microsoft-wdac-str-alert-trigger-success-3076 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_id', 'alert_name', 'dest_host', 'event_code', 'host', 'process_dir', 'process_name', 'process_path', 'time', 'user'] |
| edit_regex_field | host |  | ['\s({dest_host}({host}[\w\-.]+))\s+MSWinEventLog'] |
| added_regex_field | dest_host |  | ['\s({dest_host}({host}[\w\-.]+))\s+MSWinEventLog'] |
| removed_attribute | DupFields |  | N/A |