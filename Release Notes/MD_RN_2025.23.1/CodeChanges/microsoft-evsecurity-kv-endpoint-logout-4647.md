# Code Changes for microsoft-evsecurity-kv-endpoint-logout-4647 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['app', 'dest_host', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'time', 'user', 'user_sid'] |
| edit_regex_field | host |  | ['(?i)(((audit|success|failure)( |_)(success|audit|failure))|information)[\s,]({dest_host}({host}[\w.-]+))\s', '<?Computer>?(Name)?\s*=?\s*"*({dest_host}({host}[\w\.-]+))(\s|,|"|</Computer>|$)', 'Microsoft-Windows-Security-Auditing.*?({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)\s+(am|AM|pm|PM|({dest_host}({host}[\w.\-]+)))', '\Wdvchost=(|({dest_host}({host}.+?)))(\s+\w+=|\s*$)'] |
| edit_regex_field | time |  | ['"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\.\d+)?Z)', 'Microsoft-Windows-Security-Auditing.*?({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)\s+(am|AM|pm|PM|({dest_host}({host}[\w.\-]+)))', 'TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d\d\d\d\dZ)"', '\s(Mon|Tue|Wed|Thu|Fri|Sat|Sun) ({time}\w+ \d+ \d+:\d+:\d+ \d+)'] |
| added_regex_field | dest_host |  | ['(?i)(((audit|success|failure)( |_)(success|audit|failure))|information)[\s,]({dest_host}({host}[\w.-]+))\s', '<?Computer>?(Name)?\s*=?\s*"*({dest_host}({host}[\w\.-]+))(\s|,|"|</Computer>|$)', 'Microsoft-Windows-Security-Auditing.*?({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)\s+(am|AM|pm|PM|({dest_host}({host}[\w.\-]+)))', '\Wdvchost=(|({dest_host}({host}.+?)))(\s+\w+=|\s*$)'] |
| removed_attribute | DupFields |  | N/A |