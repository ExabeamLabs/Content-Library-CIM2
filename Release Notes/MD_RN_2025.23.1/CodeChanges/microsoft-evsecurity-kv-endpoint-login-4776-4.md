# Code Changes for microsoft-evsecurity-kv-endpoint-login-4776-4 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'event_code', 'failure_code', 'host', 'result_code', 'time', 'user'] |
| edit_regex_field | dest_host |  | ['summary_windows_4776_data="+\d+:\d+:\d+\s*\d+-\d+-\d+:::({host}[^:::]+)?:::({event_code}[^:::]+)?:::({dest_host}[\w\-.]+)?:::({failure_code}({result_code}[^:::]+))?:::({user}[\w\.\-\!\#\^\~]{1,40}\$?)?:::([^:::]+):::'] |
| edit_regex_field | event_code |  | ['({event_code}4776)', 'summary_windows_4776_data="+\d+:\d+:\d+\s*\d+-\d+-\d+:::({host}[^:::]+)?:::({event_code}[^:::]+)?:::({dest_host}[\w\-.]+)?:::({failure_code}({result_code}[^:::]+))?:::({user}[\w\.\-\!\#\^\~]{1,40}\$?)?:::([^:::]+):::'] |
| edit_regex_field | host |  | ['summary_windows_4776_data="+\d+:\d+:\d+\s*\d+-\d+-\d+:::({host}[^:::]+)?:::({event_code}[^:::]+)?:::({dest_host}[\w\-.]+)?:::({failure_code}({result_code}[^:::]+))?:::({user}[\w\.\-\!\#\^\~]{1,40}\$?)?:::([^:::]+):::'] |
| edit_regex_field | result_code |  | ['summary_windows_4776_data="+\d+:\d+:\d+\s*\d+-\d+-\d+:::({host}[^:::]+)?:::({event_code}[^:::]+)?:::({dest_host}[\w\-.]+)?:::({failure_code}({result_code}[^:::]+))?:::({user}[\w\.\-\!\#\^\~]{1,40}\$?)?:::([^:::]+):::'] |
| edit_regex_field | user |  | ['summary_windows_4776_data="+\d+:\d+:\d+\s*\d+-\d+-\d+:::({host}[^:::]+)?:::({event_code}[^:::]+)?:::({dest_host}[\w\-.]+)?:::({failure_code}({result_code}[^:::]+))?:::({user}[\w\.\-\!\#\^\~]{1,40}\$?)?:::([^:::]+):::'] |
| added_regex_field | failure_code |  | ['summary_windows_4776_data="+\d+:\d+:\d+\s*\d+-\d+-\d+:::({host}[^:::]+)?:::({event_code}[^:::]+)?:::({dest_host}[\w\-.]+)?:::({failure_code}({result_code}[^:::]+))?:::({user}[\w\.\-\!\#\^\~]{1,40}\$?)?:::([^:::]+):::'] |
| removed_attribute | DupFields |  | N/A |