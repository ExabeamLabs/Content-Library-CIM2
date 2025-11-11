# Code Changes for microsoft-evsecurity-str-endpoint-672 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'dest_ip', 'dest_port', 'domain', 'event_code', 'host', 'result_code', 'time', 'user', 'user_sid'] |
| edit_regex_field | event_code |  | ['EvntSLog:\s+\[.+\]\s+({time}\w+ \w+ \d+ \d+:\d+:\d+ \d+):\s+({dest_host}({host}[\w.\- /\\]+))\/.*\s+\(({event_code}\w+)\)'] |
| edit_regex_field | host |  | ['EvntSLog:\s+\[.+\]\s+({time}\w+ \w+ \d+ \d+:\d+:\d+ \d+):\s+({dest_host}({host}[\w.\- /\\]+))\/.*\s+\(({event_code}\w+)\)'] |
| edit_regex_field | time |  | ['EvntSLog:\s+\[.+\]\s+({time}\w+ \w+ \d+ \d+:\d+:\d+ \d+):\s+({dest_host}({host}[\w.\- /\\]+))\/.*\s+\(({event_code}\w+)\)'] |
| added_regex_field | dest_host |  | ['EvntSLog:\s+\[.+\]\s+({time}\w+ \w+ \d+ \d+:\d+:\d+ \d+):\s+({dest_host}({host}[\w.\- /\\]+))\/.*\s+\(({event_code}\w+)\)'] |
| removed_attribute | DupFields |  | N/A |