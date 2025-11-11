# Code Changes for microsoft-evsecurity-kv-handle-request-success-4659 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'object', 'object_id', 'object_server', 'object_type', 'process_id', 'time', 'user', 'user_sid'] |
| edit_regex_field | host |  | ['(?i)(((audit|success|failure)( |_)(success|audit|failure))|information)[\s,]({dest_host}({host}[\w.-]+))', '<?Computer>?(Name)?\s*=?\s*"*({dest_host}({host}[\w\.-]+))(\s|,|"|</Computer>|$)', 'Microsoft-Windows-Security-Auditing.*?({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)\s+(am|AM|pm|PM|({dest_host}({host}[\w.\-]+)))', '\Wdvchost=(|({dest_host}({host}.+?)))(\s+\w+=|\s*$)'] |
| edit_regex_field | time |  | ['Microsoft-Windows-Security-Auditing.*?({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)\s+(am|AM|pm|PM|({dest_host}({host}[\w.\-]+)))'] |
| added_regex_field | dest_host |  | ['(?i)(((audit|success|failure)( |_)(success|audit|failure))|information)[\s,]({dest_host}({host}[\w.-]+))', '<?Computer>?(Name)?\s*=?\s*"*({dest_host}({host}[\w\.-]+))(\s|,|"|</Computer>|$)', 'Microsoft-Windows-Security-Auditing.*?({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)\s+(am|AM|pm|PM|({dest_host}({host}[\w.\-]+)))', '\Wdvchost=(|({dest_host}({host}.+?)))(\s+\w+=|\s*$)'] |
| removed_attribute | DupFields |  | N/A |