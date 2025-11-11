# Code Changes for microsoft-wdac-str-endpoint-notification-success-3099 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_id', 'dest_host', 'event_code', 'event_name', 'host', 'result_code', 'time', 'user'] |
| edit_regex_field | host |  | ['\s({dest_host}({host}[\w\-.]+))\s+MSWinEventLog'] |
| added_regex_field | dest_host |  | ['\s({dest_host}({host}[\w\-.]+))\s+MSWinEventLog'] |
| removed_attribute | DupFields |  | N/A |