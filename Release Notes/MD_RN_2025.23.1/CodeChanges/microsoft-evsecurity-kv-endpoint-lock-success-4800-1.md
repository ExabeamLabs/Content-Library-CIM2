# Code Changes for microsoft-evsecurity-kv-endpoint-lock-success-4800-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'time', 'user'] |
| edit_regex_field | host |  | ['(?i)(((audit|success)( |_)(success|audit))|information)(<\d+>|\s+)({dest_host}({host}[\w\-.]+))', 'Computer(\w+)?[\"\s]*(:|=)\s*\"?({dest_host}({host}[\w\-.]+?))(\"|\s)', 'Microsoft-Windows-Security-Auditing.*?({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)\s+(am|AM|pm|PM|({dest_host}({host}[\w.\-]+)))'] |
| edit_regex_field | time |  | ['"TimeCreated":"[\\\/]*Date\(({time}\d{13})', '(Mon|Tue|Wed|Thu|Fri|Sat|Sun) ({time}\w+ \d+ \d+:\d+:\d+ \d+)', '({time}\d\d\/\d\d\/\d\d\d\d\s+\d\d:\d\d:\d\d\s+(?i)(AM|PM))', '({time}\w{3}\s\d{2}\s\d{2}:\d{2}:\d{2}\s\d{4})', 'Microsoft-Windows-Security-Auditing.*?({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)\s+(am|AM|pm|PM|({dest_host}({host}[\w.\-]+)))'] |
| added_regex_field | dest_host |  | ['(?i)(((audit|success)( |_)(success|audit))|information)(<\d+>|\s+)({dest_host}({host}[\w\-.]+))', 'Computer(\w+)?[\"\s]*(:|=)\s*\"?({dest_host}({host}[\w\-.]+?))(\"|\s)', 'Microsoft-Windows-Security-Auditing.*?({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)\s+(am|AM|pm|PM|({dest_host}({host}[\w.\-]+)))'] |
| removed_attribute | DupFields |  | N/A |