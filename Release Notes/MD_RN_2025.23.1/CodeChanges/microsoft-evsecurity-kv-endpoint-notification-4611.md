# Code Changes for microsoft-evsecurity-kv-endpoint-notification-4611 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'process_name', 'time', 'user', 'user_sid'] |
| edit_regex_field | host |  | ['\w+\s+\d+\s+\d+:\d+:\d+\s+({dest_host}({host}[\w\-.]+))\s+MSWinEventLog', '\w+\s{1,2}\d{1,2}\s\d\d:\d\d:\d\d\s(\d{4}|({dest_host}({host}[\w\-.]+)))\s\w+'] |
| added_regex_field | dest_host |  | ['\w+\s+\d+\s+\d+:\d+:\d+\s+({dest_host}({host}[\w\-.]+))\s+MSWinEventLog', '\w+\s{1,2}\d{1,2}\s\d\d:\d\d:\d\d\s(\d{4}|({dest_host}({host}[\w\-.]+)))\s\w+'] |
| removed_attribute | DupFields |  | N/A |