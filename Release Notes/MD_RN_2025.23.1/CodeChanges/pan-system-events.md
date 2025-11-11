# Code Changes for pan-system-events (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'event_name', 'host', 'src_ip', 'time', 'user'] |
| edit_regex_field | event_name |  | ['\d\d:\d\d ({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}) .+?({time}\w+ \d+ \d\d\d\d \d\d:\d\d:\d\d),([^,]*,){3}({event_name}[^,]+),({dest_host}({host}[^,]+)),(|({user}[\w\.\-\!\#\^\~]{1,40}\$?)),'] |
| edit_regex_field | host |  | ['\d\d:\d\d ({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}) .+?({time}\w+ \d+ \d\d\d\d \d\d:\d\d:\d\d),([^,]*,){3}({event_name}[^,]+),({dest_host}({host}[^,]+)),(|({user}[\w\.\-\!\#\^\~]{1,40}\$?)),'] |
| edit_regex_field | src_ip |  | ['\d\d:\d\d ({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}) .+?({time}\w+ \d+ \d\d\d\d \d\d:\d\d:\d\d),([^,]*,){3}({event_name}[^,]+),({dest_host}({host}[^,]+)),(|({user}[\w\.\-\!\#\^\~]{1,40}\$?)),'] |
| edit_regex_field | time |  | ['((?:1969-[^,]+?)|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-]\d+:\d+))', '\d\d:\d\d ({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}) .+?({time}\w+ \d+ \d\d\d\d \d\d:\d\d:\d\d),([^,]*,){3}({event_name}[^,]+),({dest_host}({host}[^,]+)),(|({user}[\w\.\-\!\#\^\~]{1,40}\$?)),'] |
| edit_regex_field | user |  | ['\d\d:\d\d ({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}) .+?({time}\w+ \d+ \d\d\d\d \d\d:\d\d:\d\d),([^,]*,){3}({event_name}[^,]+),({dest_host}({host}[^,]+)),(|({user}[\w\.\-\!\#\^\~]{1,40}\$?)),'] |
| added_regex_field | dest_host |  | ['\d\d:\d\d ({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}) .+?({time}\w+ \d+ \d\d\d\d \d\d:\d\d:\d\d),([^,]*,){3}({event_name}[^,]+),({dest_host}({host}[^,]+)),(|({user}[\w\.\-\!\#\^\~]{1,40}\$?)),'] |
| removed_attribute | DupFields |  | N/A |